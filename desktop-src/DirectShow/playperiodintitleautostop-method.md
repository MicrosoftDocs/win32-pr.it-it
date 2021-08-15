---
description: Il metodo PlayPeriodInTitleAutoStop avvia la riproduzione all'ora specificata nel titolo specificato fino all'ora di arresto specificata.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Metodo PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dbf0a5c157efcf4d22e7e5ba650bfdfebc57fe6a43d319e0be14958d732024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564061"
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

Specifica il titolo come integer.

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*
</dt> <dd>

Specifica l'ora di inizio come stringa nel formato "hh:mm:ss:ff" (specificando ore, minuti, secondi, fotogrammi).

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*
</dt> <dd>

Specifica l'ora di fine come stringa nel formato "hh:mm:ss:ff".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayChaptersAutoStop**](playchaptersautostop-method.md)
</dt> </dl>

 

 



