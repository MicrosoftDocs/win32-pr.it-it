---
description: Il metodo GetGPRM recupera il registro dei parametri generali specificato.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Metodo GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c46307f1cbec49b4916cdbd528c2b22cfb42bf89a06285c5c779339786599d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812561"
---
# <a name="getgprm-method"></a>Metodo GetGPRM

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetGPRM` metodo recupera il registro dei parametri generali specificato.

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*Iindex*
</dt> <dd>

Specifica il registro da recuperare come integer. Il valore deve essere compreso tra 0 e 15.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il registro specificato.

## <a name="remarks"></a>Commenti

Questo metodo non è necessario per le funzionalità di navigazione o riproduzione di DVD che usano **l'oggetto MSWebDVD.** Viene fornito per gli utenti con una conoscenza approfondita della specifica DVD che vogliono implementare funzionalità avanzate. Le GPPM possono essere usate per contenere qualsiasi valore, in modo che possano essere impostate e lette liberamente. Tuttavia, poiché le GPRM vengono usate anche per archiviare i comandi del disco, la modifica dei valori tramite [**SetGPRM**](setgprm-method.md) può comportare un comportamento imprevedibile.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



