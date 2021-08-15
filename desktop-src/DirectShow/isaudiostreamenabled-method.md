---
description: Il metodo IsAudioStreamEnabled recupera un valore che indica se il flusso audio specificato è abilitato nel titolo corrente.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Metodo IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2131376346f2a0311fc5acd8e0051292a12fb0145b44226363c7d891a5ef3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817476"
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

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Specifica il flusso audio come valore Intero compreso tra 0 e 7.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se il flusso audio specificato è disponibile per il titolo corrente. True indica che è disponibile.

## <a name="remarks"></a>Commenti

Anche se un disco può contenere fino a otto flussi audio indipendenti, ogni flusso non è necessariamente disponibile per ogni titolo. Ad esempio, un titolo di film principale potrebbe avere tre flussi audio per l'inglese, lo spagnolo e il giapponese, ma il titolo "ComingAs" potrebbe avere un solo flusso audio in inglese. Verificare sempre che un flusso sia disponibile per un titolo prima di impostare la [**proprietà CurrentAudioStream.**](currentaudiostream-property.md)

 

 



