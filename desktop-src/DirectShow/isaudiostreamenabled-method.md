---
description: Il metodo IsAudioStreamEnabled recupera un valore che indica se il flusso audio specificato è abilitato nel titolo corrente.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Metodo IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520394"
---
# <a name="isaudiostreamenabled-method"></a>Metodo IsAudioStreamEnabled

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `IsAudioStreamEnabled` metodo recupera un valore che indica se il flusso audio specificato è abilitato nel titolo corrente.

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Specifica il flusso audio come valore intero compreso tra 0 e 7.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se il flusso audio specificato è disponibile per il titolo corrente. True indica che è disponibile.

## <a name="remarks"></a>Commenti

Sebbene un disco possa contenere fino a otto flussi audio indipendenti, ogni flusso non è necessariamente disponibile per ogni titolo. Un titolo di film principale, ad esempio, potrebbe avere tre flussi audio per l'inglese, spagnolo e giapponese, ma il titolo "attractions" potrebbe avere un solo flusso audio in inglese. Verificare sempre che un flusso sia disponibile per un titolo prima di impostare la proprietà [**CurrentAudioStream**](currentaudiostream-property.md) .

 

 



