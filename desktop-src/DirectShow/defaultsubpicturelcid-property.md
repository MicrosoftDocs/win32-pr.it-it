---
description: La proprietà DVDAdm.DefaultSubpictureLCID imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per il flusso di immagini secondarie.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Proprietà DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc67be112349a050df45f625fda6488c91b22dee357c820724de5842c156894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952990"
---
# <a name="defaultsubpicturelcid-property"></a>Proprietà DefaultSubpictureLCID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DefaultSubpictureLCID` proprietà imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per il flusso di immagini secondarie.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore Integer che rappresenta l'LCID dell'immagine secondaria predefinita specificata dall'utente come archiviato nelle impostazioni del Registro di sistema per l'applicazione DVD. Questo valore non corrisponde necessariamente al flusso di immagini secondarie predefinito creato nel DVD. Per l'intervallo di PID validi, vedere la documentazione di Win32 in Platform SDK.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura senza alcun valore predefinito. Se non viene specificato alcun LCID dell'immagine secondaria predefinita, l'oggetto MSDVDAdm riprodurrà il flusso di immagini secondarie contrassegnato come flusso predefinito sul disco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



