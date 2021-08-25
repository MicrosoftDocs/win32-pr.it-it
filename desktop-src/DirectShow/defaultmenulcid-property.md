---
description: La proprietà DVDAdm.DefaultMenuLCID imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per i menu.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Proprietà DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 939f65ad41cb184f38e2a30392030ca67066fe203f7952441cc2f77b1db95242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906891"
---
# <a name="defaultmenulcid-property"></a>Proprietà DefaultMenuLCID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DefaultMenuLCID` proprietà imposta o recupera l'impostazione del Registro di sistema per l'identificatore LCID predefinito specificato dall'utente per i menu.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore Integer che rappresenta l'LCID archiviato nelle impostazioni del Registro di sistema per l'applicazione DVD. Questo valore non corrisponde necessariamente alla lingua di menu predefinita, come è stato creato nel DVD. Per la gamma di CID validi, vedere la documentazione di Win32 in Platform SDK.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura senza alcun valore predefinito. Se non viene specificato alcun LCID del menu predefinito, l'oggetto MSDVDAdm userà la lingua contrassegnata come lingua di menu predefinita sul disco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



