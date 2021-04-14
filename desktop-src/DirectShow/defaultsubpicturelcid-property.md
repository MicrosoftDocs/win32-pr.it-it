---
description: La proprietà DVDAdm. DefaultSubpictureLCID imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso di immagine.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Proprietà DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522785"
---
# <a name="defaultsubpicturelcid-property"></a>Proprietà DefaultSubpictureLCID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DefaultSubpictureLCID` proprietà imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso dell'immagine.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta l'LCID della sottoimmagine predefinita specificato dall'utente come archiviato nelle impostazioni del registro di sistema per l'applicazione DVD. Questo valore non è necessariamente lo stesso del flusso di immagine predefinita come creato nel DVD. Per l'intervallo degli LCID validi, vedere la documentazione di Win32 in Platform SDK.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito. Se non viene specificato alcun LCID della sottoimmagine predefinita, l'oggetto MSDVDAdm riprodurrà il flusso dell'immagine subpicture contrassegnato come flusso predefinito sul disco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



