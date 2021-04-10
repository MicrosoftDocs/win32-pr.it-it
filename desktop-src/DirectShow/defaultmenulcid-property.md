---
description: La proprietà DVDAdm. DefaultMenuLCID imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per i menu.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Proprietà DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125175"
---
# <a name="defaultmenulcid-property"></a>Proprietà DefaultMenuLCID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DefaultMenuLCID` proprietà imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per i menu.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta l'LCID come archiviato nelle impostazioni del registro di sistema per l'applicazione DVD. Questo valore non è necessariamente uguale alla lingua di menu predefinita creata sul DVD. Per l'intervallo degli LCID validi, vedere la documentazione di Win32 in Platform SDK.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito. Se non viene specificato alcun LCID di menu predefinito, l'oggetto MSDVDAdm utilizzerà la lingua contrassegnata come lingua di menu predefinita sul disco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



