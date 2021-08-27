---
title: Tipi di esclusione reciproca
description: Tipi di esclusione reciproca
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows Media Format SDK, esclusione reciproca
- Advanced Systems Format (ASF), esclusione reciproca
- ASF (Advanced Systems Format), esclusione reciproca
- esclusione reciproca, tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da546c753696144c68348c61d01473c7d6414290b5971c220ac8c983317b3b15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110271"
---
# <a name="mutual-exclusion-types"></a>Tipi di esclusione reciproca

È possibile usare i tipi di esclusione reciproca per identificare la natura di un oggetto di esclusione reciproca in un profilo. I tipi di esclusione reciproca vengono usati come parametri [**per IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) e [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).

Nella tabella seguente sono elencati gli identificatori per i tipi di esclusione reciproca.



| Costante del tipo di esclusione reciproca | GUID                                 |
|--------------------------------|--------------------------------------|
| Linguaggio \_ CLSID \_ WMMUTEX       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| Velocità in bit \_ CLSID WMMUTEX \_        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| Presentazione DI \_ CLSID \_ WMMUTEX   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ Sconosciuto        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Valori GUID**](guid-values.md)
</dt> </dl>

 

 




