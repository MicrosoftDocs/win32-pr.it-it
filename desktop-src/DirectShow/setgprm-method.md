---
description: Il metodo SetGPRM imposta il registro del parametro generale specificato sul valore specificato.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Metodo SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303896"
---
# <a name="setgprm-method"></a>Metodo SetGPRM

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SetGPRM` metodo imposta il registro del parametro generale specificato sul valore specificato.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Specifica il registro del parametro generale da impostare come Integer. Il valore intero deve essere compreso tra 0 e 15.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*
</dt> <dd>

Specifica il nuovo valore per il registro come intero.

</dd> </dl>

## <a name="remarks"></a>Commenti

I registri di parametri generali, o GPRMs, sono registri a 16 bit che ciascun disco può usare in modo univoco per l'archiviazione temporanea dei dati. Non è necessario che un'applicazione del lettore acceda a questi registri per qualsiasi controllo di riproduzione o navigazione standard usando l'oggetto **mswebdvd** . Questo metodo viene fornito per le applicazioni del lettore che implementano funzionalità avanzate. Non tentare di modificare direttamente il GPRMs, a meno che non si disponga di una conoscenza approfondita della specifica DVD e delle modalità di utilizzo di GPRMs sul disco specifico da riprodurre. La modifica di questi valori può causare un comportamento imprevedibile.

 

 



