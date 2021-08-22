---
description: Il metodo GetSubpictureLanguage recupera la lingua per il flusso di immagini secondarie specificato.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Metodo GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdedc90789efb331b1438744a0f64a42782bf1d1e363170ce626ed023d2e542a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536931"
---
# <a name="getsubpicturelanguage-method"></a>Metodo GetSubpictureLanguage

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetSubpictureLanguage` metodo recupera la lingua per il flusso di immagini secondarie specificato.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Specifica il numero del flusso di immagini secondarie di cui si vuole recuperare la lingua di testo come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa leggibile che identifica la lingua del flusso audio nel titolo corrente.

 

 



