---
description: Il metodo GetAudioLanguage recupera una stringa che indica la lingua disponibile nel flusso audio specificato.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Metodo GetAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f4842e370a11fde655ee1695e56dc148f9ebece2de01969b2603225efad7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000381"
---
# <a name="getaudiolanguage-method"></a>Metodo GetAudioLanguage

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetAudioLanguage` metodo recupera una stringa che indica la lingua disponibile nel flusso audio specificato.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Specifica il numero del flusso audio nel titolo corrente come Integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa leggibile dall'utente che identifica la lingua del flusso audio nel titolo corrente.

 

 



