---
description: Il metodo GetSubpictureLanguage recupera la lingua per il flusso di sottoimmagine specificato.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Metodo GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303742"
---
# <a name="getsubpicturelanguage-method"></a>Metodo GetSubpictureLanguage

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetSubpictureLanguage` metodo recupera la lingua per il flusso di sottoimmagine specificato.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Specifica il numero del flusso dell'immagine di sottoimmagine di cui si desidera recuperare la lingua del testo come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa leggibile che identifica la lingua del flusso audio nel titolo corrente.

 

 



