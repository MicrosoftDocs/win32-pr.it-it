---
description: Descrive le strutture usate dalle interfacce video Microsoft Direct3D 9.
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Strutture video Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ac8e03ff524f7f943c6adbee39b57785112a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305399"
---
# <a name="direct3d-9-video-structures"></a>Strutture video Direct3D 9

Descrive le strutture usate dalle interfacce video Microsoft Direct3D 9.



| Struttura                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_OMAC D3D**](d3d-omac.md)<br/> Contiene un Message Authentication Code (MAC).<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAES \_ CTR \_ IV**](d3daes-ctr-iv.md)<br/> Contiene un vettore di inizializzazione (IV).<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ configurare l' \_ input**](d3dauthenticatedchannel-configure-input.md)<br/> Contiene i dati di input per il metodo [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ configurare l' \_ output**](d3dauthenticatedchannel-configure-output.md)<br/> Contiene la risposta a una chiamata al metodo [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                        |
| [**\_CONFIGUREINITIALIZE D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configureinitialize.md)<br/> Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .<br/>                                                                                                                       |
| [**\_CONFIGUREPROTECTION D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configureprotection.md)<br/> Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ Protection**](d3dauthenticatedconfigure-protection.md) .<br/>                                                                                                                       |
| [**\_CONFIGURECRYPTOSESSION D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configurecryptosession.md)<br/> Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .<br/>                                                                                                           |
| [**\_CONFIGURESHAREDRESOURCE D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configuresharedresource.md)<br/> Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .<br/>                                                                                                       |
| [**\_CONFIGUREUNCOMPRESSEDENCRYPTION D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> Contiene i dati di input per un comando [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .<br/>                                                                   |
| [**\_Flag di protezione D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-protection-flags.md)<br/> Specifica il livello di protezione per il contenuto video.<br/>                                                                                                                                                                                                   |
| [**\_Input query \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)<br/> Contiene i dati di input per il metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                                     |
| [**\_Output della query D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-output.md)<br/> Contiene la risposta a una chiamata al metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                        |
| [**\_Output QUERYCHANNELTYPE \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) .<br/>                                                                                                                     |
| [**\_Input QUERYCRYPTOSESSION \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> Contiene i dati di input per una query [**\_ CRYPTOSESSION D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                                |
| [**\_Output QUERYCRYPTOSESSION \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                             |
| [**\_Output QUERYDEVICEHANDLE \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) .<br/>                                                                                                                 |
| [**\_Input QUERYEVICTIONENCRYPTIONGUID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> Contiene i dati di input per una query [**\_ ENCRYPTIONWHENACCESSIBLEGUID D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                                |
| [**\_Output QUERYEVICTIONENCRYPTIONGUID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                             |
| [**\_Output QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .<br/>                                         |
| [**\_Output QUERYINFOBUSTYPE \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) .<br/>                                                                                             |
| [**\_Input QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> Contiene dati intput per una [**query \_ OUTPUTID D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                   |
| [**\_Output QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                 |
| [**\_Input QUERYOUTPUTIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> Contiene i dati di input per una query [**\_ OUTPUTIDCOUNT D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                                |
| [**\_Output QUERYOUTPUTIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                             |
| [**\_Output QUERYPROTECTION \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryprotection-output.md)<br/> Contiene la risposta a una query di [**\_ protezione D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .<br/>                                                                                                                         |
| [**\_Input QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> Contiene i dati di input per una query [**\_ RESTRICTEDSHAREDRESOURCEPROCESS D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                        |
| [**\_Output QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                     |
| [**\_Output QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .<br/>                 |
| [**\_Output QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) .<br/>                                             |
| [**\_Output QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> Contiene la risposta a una query [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> Descrive le funzionalità di protezione del contenuto di un driver di visualizzazione.<br/>                                                                                                                                                                                                                    |
| [**\_Informazioni blocco \_ D3DENCRYPTED**](d3dencrypted-block-info.md)<br/> Specifica i byte crittografati in una superficie video protetta.<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> Specifica le funzionalità di sovrapposizione hardware per un dispositivo Direct3D.<br/>                                                                                                                                                                                                                                            |
| [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> Specifica un buffer per il metodo [**IDirect3DDXVADevice9:: Execute**](idirect3ddxvadevice9-execute.md) .<br/>                                                                                                                                                                                                  |
| [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> Specifica i requisiti per le superfici compresse per l'accelerazione video DirectX (DXVA).<br/>                                                                                                                                                                                                         |
| [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> Specifica le dimensioni e il formato pixel delle superfici non compresse per la decodifica video DXVA.<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API video Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




