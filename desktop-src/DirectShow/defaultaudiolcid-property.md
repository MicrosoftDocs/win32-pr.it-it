---
description: La proprietà DVDAdm.DefaultAudioLCID imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Proprietà DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7ebcd864f8ac3bff8cfd8556703dd091985a72c0dfea4f0eefb9f974213165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953007"
---
# <a name="defaultaudiolcid-property"></a>Proprietà DefaultAudioLCID

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.DefaultAudioLCID` proprietà imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore Integer che rappresenta l'LCID audio predefinito specificato dall'utente come archiviato nelle impostazioni del Registro di sistema per l'applicazione DVD. Questo valore non corrisponde necessariamente al flusso audio predefinito creato nel DVD.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura senza alcun valore predefinito. Se non viene specificato alcun LCID audio predefinito, l'oggetto MSDVDAdm riprodurrà il flusso audio contrassegnato come flusso predefinito sul disco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



