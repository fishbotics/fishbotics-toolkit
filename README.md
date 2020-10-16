# fishbotics-toolkit
Example usage
```
urdf_file = /PATH/TO/URDF/FILE
device = torch.device('cuda')
# You have to pass in the device on construction
robot = TorchURDF.load(urdf_file, device)
# Configurations are passed in batch
cfgs = torch.zeros((batch_size, configuration_size))

# fk returned will be a dictionary with keys being the link names and the
# values being a batched transformation matrix from the
# link's frame into the world frame
fk = self.robot.link_fk_batch(cfgs, device, use_names=True)
```
