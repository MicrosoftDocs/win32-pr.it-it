---
description: La proprietà DVDAdm. DefaultAudioLCID imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Proprietà DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304202"
---
# <a name="defaultaudiolcid-property"></a>Proprietà DefaultAudioLCID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DefaultAudioLCID` proprietà imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta l'LCID audio predefinito specificato dall'utente come archiviato nelle impostazioni del registro di sistema per l'applicazione DVD. Questo valore non è necessariamente uguale al flusso audio predefinito creato nel DVD.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito. Se non viene specificato alcun LCID audio predefinito, l'oggetto MSDVDAdm riprodurrà il flusso audio contrassegnato come flusso predefinito sul disco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



