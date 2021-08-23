---
description: Elenca le query per il metodo IDirect3DAuthenticatedChannel9::Query.
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: protezione del contenuto query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5aaa8c43cf722d13550ab4a1860e7a53780e7e82da7f374e28a7f599a22638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829091"
---
# <a name="content-protection-queries"></a>protezione del contenuto query

Elenca le query per il [**metodo IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)



| Richiesta di stato                                                                                                                            | Descrizione                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Restituisce il tipo di bus di I/O utilizzato per inviare dati alla GPU.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md)                                                           | Restituisce il tipo di canale autenticato.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Restituisce handle alla sessione di crittografia e al dispositivo Direct3D associati a un dispositivo decodificatore DirectX Video Acceleration 2 (DXVA-2) specificato. |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Restituisce il tipo di crittografia applicato prima che il contenuto diventi accessibile alla CPU o al bus.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | Restituisce un handle al dispositivo associato a questo canale autenticato.                                                                          |
| [**CRITTOGRAFIA D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUID \_**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Restituisce uno dei tipi di crittografia che possono essere usati per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.                                     |
| [**CRITTOGRAFIA D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUIDCOUNT \_**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Restituisce il numero di tipi di crittografia che possono essere usati per crittografare il contenuto prima che diventi accessibile alla CPU o al bus.                                  |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md)                                                                 | Restituisce uno degli identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | Restituisce il numero di identificatori di output associati a una sessione di crittografia e a un dispositivo Direct3D specificati.                                             |
| [**PROTEZIONE D3DAUTHENTICATEDQUERY \_**](d3dauthenticatedquery-protection.md)                                                             | Restituisce il livello di protezione corrente per il dispositivo.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Restituisce informazioni su un processo a cui è consentito aprire risorse condivise con accesso limitato.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Restituisce il numero di processi autorizzati ad aprire risorse condivise con accesso limitato.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Restituisce il numero di risorse condivise protette che possono essere aperte da qualsiasi processo senza restrizioni.                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API Video Direct3D](direct3d-video-apis.md)
</dt> <dt>

[Criteri basati su GPU protezione del contenuto](gpu-based-content-protection.md)
</dt> </dl>

 

 



