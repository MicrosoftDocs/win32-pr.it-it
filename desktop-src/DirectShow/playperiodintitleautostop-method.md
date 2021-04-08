---
description: Il metodo PlayPeriodInTitleAutoStop avvia la riproduzione all'ora specificata nel titolo specificato fino all'ora di arresto specificata.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Metodo PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876373"
---
# <a name="playperiodintitleautostop-method"></a>Metodo PlayPeriodInTitleAutoStop

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayPeriodInTitleAutoStop` metodo avvia la riproduzione all'ora specificata nel titolo specificato fino all'ora di arresto specificata.

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Specifica il titolo come intero.

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*
</dt> <dd>

Specifica l'ora di inizio come stringa nel formato "HH: mm: SS: FF" (specifica di ore, minuti, secondi, frame).

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*
</dt> <dd>

Specifica l'ora di fine come stringa nel formato "HH: mm: SS: FF".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayChaptersAutoStop**](playchaptersautostop-method.md)
</dt> </dl>

 

 



