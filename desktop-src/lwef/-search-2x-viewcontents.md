---
title: Enumerazione ViewContents
description: Utilizzato dal contenuto IResultsViewer per indicare o impostare il modo in cui viene visualizzato il set restituito della query corrente.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione ViewContents
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
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333634"
---
# <a name="viewcontents-enumeration"></a>Enumerazione ViewContents

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Usato da [**IResultsViewer:: Contents**](-search-2x-iresultsviewer-contents.md) per indicare o impostare il modo in cui viene visualizzato il set restituito della query corrente.

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

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**
</dt> <dd>

Indica il tipo di contenuto visualizzato nella visualizzazione dei risultati.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**
</dt> <dd>

Indica che il tipo di contenuto visualizzato nella visualizzazione risultati è attualmente impostato sulla visualizzazione Shell.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

Indica che il tipo di contenuto visualizzato nella visualizzazione dei risultati è attualmente impostato sulla visualizzazione del browser.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





