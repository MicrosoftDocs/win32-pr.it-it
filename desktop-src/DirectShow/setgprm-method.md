---
description: Il metodo SetGPRM imposta il registro dei parametri generali specificato sul valore specificato.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Metodo SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c217f0235ca5b055e20102f553e9e23f5b93e6dd9c3d74db560584690a669ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078861"
---
# <a name="setgprm-method"></a>Metodo SetGPRM

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SetGPRM` metodo imposta il registro dei parametri generali specificato sul valore specificato.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*Iindex*
</dt> <dd>

Specifica il registro dei parametri generale da impostare come integer. Il valore Integer deve essere compreso tra 0 e 15.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*
</dt> <dd>

Specifica il nuovo valore per il registro come integer.

</dd> </dl>

## <a name="remarks"></a>Commenti

I registri dei parametri generali, o GPRM, sono registri a 16 bit che ogni disco può usare in modo univoco per l'archiviazione temporanea dei dati. Un'applicazione lettore non deve accedere a questi registri per qualsiasi controllo di riproduzione o navigazione standard usando **l'oggetto MSWebDVD.** Questo metodo viene fornito per le applicazioni lettore che implementano funzionalità avanzate. Non tentare di modificare direttamente i GPRM a meno che non si abbia una conoscenza approfondita della specifica DVD e dei modi in cui i GPRIM vengono usati sul disco specifico da riprodurre. La modifica di questi valori può comportare un comportamento imprevedibile.

 

 



