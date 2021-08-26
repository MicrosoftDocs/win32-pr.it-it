---
title: Tipi di condivisione della larghezza di banda
description: Tipi di condivisione della larghezza di banda
ms.assetid: 2da15981-65d4-4d77-a68c-810ded18670c
keywords:
- Windows MEDIA Format SDK, condivisione della larghezza di banda
- Advanced Systems Format (ASF), condivisione della larghezza di banda
- ASF (Advanced Systems Format),bandwidth sharing
- condivisione della larghezza di banda, tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf2b9ea05210e39c54334373be725284dbd1affc0170be6568600eeb4c2bead
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055591"
---
# <a name="bandwidth-sharing-types"></a>Tipi di condivisione della larghezza di banda

È possibile usare i tipi di condivisione della larghezza di banda per identificare la natura di un oggetto di condivisione della larghezza di banda in un profilo. I tipi di condivisione della larghezza di banda vengono usati come parametri per [**IWMBandwidthSharing::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-gettype) e [**IWMBandwidthSharing::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-settype).

Nella tabella seguente sono elencati gli identificatori per i tipi di condivisione della larghezza di banda.



| Costante del tipo di condivisione della larghezza di banda      | GUID                                 |
|--------------------------------------|--------------------------------------|
| CLSID \_ WMBandwidthSharing \_ Exclusive | af6060aa-5197-11d2-b6af-00c04fd908e9 |
| CLSID \_ WMBandwidthSharing \_ Partial   | af6060ab-5197-11d2-b6af-00c04fd908e9 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Valori GUID**](guid-values.md)
</dt> </dl>

 

 




