---
title: Tipi di esclusione reciproca
description: Tipi di esclusione reciproca
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows Media Format SDK, esclusione reciproca
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- esclusione reciproca, tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046268"
---
# <a name="mutual-exclusion-types"></a>Tipi di esclusione reciproca

È possibile utilizzare i tipi di esclusione reciproca per identificare la natura di un oggetto di esclusione reciproca in un profilo. I tipi di esclusione reciproca vengono usati come parametri per [**IWMMutualExclusion:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) e [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).

Nella tabella seguente sono elencati gli identificatori per i tipi di esclusione reciproca.



| Costante tipo di esclusione reciproca | GUID                                 |
|--------------------------------|--------------------------------------|
| \_Lingua WMMUTEX \_ CLSID       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| \_ \_ Bitrate WMMUTEX CLSID        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| \_Presentazione WMMUTEX \_ CLSID   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ sconosciuto        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Valori GUID**](guid-values.md)
</dt> </dl>

 

 




