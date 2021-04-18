---
description: 'Elenca le query per il metodo IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Query di protezione del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a72f7f054783a644cb352727f4bf65864bf5f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305473"
---
# <a name="content-protection-queries"></a>Query di protezione del contenuto

Elenca le query per il metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .



| Richiesta di stato                                                                                                                            | Descrizione                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACCESSIBILITYATTRIBUTES D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Restituisce il tipo di bus di I/O utilizzato per inviare i dati alla GPU.                                                                                                   |
| [**\_CHANNELTYPE D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-channeltype.md)                                                           | Restituisce il tipo di canale autenticato.                                                                                                                  |
| [**\_CRYPTOSESSION D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-cryptosession.md)                                                       | Restituisce handle per la sessione di crittografia e il dispositivo Direct3D associati a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) specificato. |
| [**\_CURRENTENCRYPTIONWHENACCESSIBLE D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Restituisce il tipo di crittografia applicato prima che il contenuto diventi accessibile alla CPU o al bus.                                                            |
| [**\_DEVICEHANDLE D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-devicehandle.md)                                                         | Restituisce un handle per il dispositivo associato a questo canale autenticato.                                                                          |
| [**\_ENCRYPTIONWHENACCESSIBLEGUID D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Restituisce uno dei tipi di crittografia che è possibile usare per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.                                     |
| [**\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Restituisce il numero di tipi di crittografia che è possibile usare per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.                                  |
| [**\_OUTPUTID D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md)                                                                 | Restituisce uno degli identificatori di output associato a una sessione di crittografia e a un dispositivo Direct3D specificati.                                        |
| [**\_OUTPUTIDCOUNT D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputidcount.md)                                                       | Restituisce il numero di identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.                                             |
| [**\_Protezione D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md)                                                             | Restituisce il livello di protezione corrente per il dispositivo.                                                                                                        |
| [**\_RESTRICTEDSHAREDRESOURCEPROCESS D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Restituisce informazioni su un processo autorizzato ad aprire risorse condivise con accesso limitato.                                                        |
| [**\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Restituisce il numero di processi a cui è consentito aprire risorse condivise con accesso limitato.                                                           |
| [**\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Restituisce il numero di risorse condivise protette che possono essere aperte da qualsiasi processo senza restrizioni.                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API video Direct3D](direct3d-video-apis.md)
</dt> <dt>

[protezione del contenuto basate su GPU](gpu-based-content-protection.md)
</dt> </dl>

 

 



