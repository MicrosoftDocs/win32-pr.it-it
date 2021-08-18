---
title: Enumerazione ViewContents
description: Usato da IResultsViewer Contents per indicare o impostare la modalità di visualizzazione del set restituito della query corrente.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Enumerazione ViewContents Funzionalità dell'Windows legacy
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2070b68ec62a8dd6ca86758b98a6399ee41180eaad24613d17d0825a927b1871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829111"
---
# <a name="viewcontents-enumeration"></a>Enumerazione ViewContents

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Usato da [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) per indicare o impostare la modalità di visualizzazione del set restituito della query corrente.

## <a name="syntax"></a>Sintassi


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**RisultatiVisualizzazione**
</dt> <dd>

Indica il tipo di contenuto visualizzato nella visualizzazione risultati.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**
</dt> <dd>

Indica che il tipo di contenuto visualizzato nella visualizzazione risultati è attualmente impostato sulla visualizzazione Shell.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

Indica che il tipo di contenuto visualizzato nella visualizzazione risultati è attualmente impostato sulla visualizzazione del browser.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView.idl</dt> </dl> |



 

 





