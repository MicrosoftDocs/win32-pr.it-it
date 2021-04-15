---
description: Il metodo GetGPRM Recupera il registro del parametro generale specificato.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Metodo GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522313"
---
# <a name="getgprm-method"></a>Metodo GetGPRM

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetGPRM` metodo recupera il registro del parametro generale specificato.

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Specifica il registro da recuperare come Integer. Il valore deve essere compreso tra 0 e 15.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il registro specificato.

## <a name="remarks"></a>Commenti

Questo metodo non è necessario per le funzionalità di navigazione o riproduzione DVD con l'oggetto **mswebdvd** . Viene fornito per gli utenti con una conoscenza approfondita della specifica DVD che desiderano implementare funzionalità avanzate. GPRMs può essere usato per contenere qualsiasi valore, in modo che possano essere impostati e letti liberamente. Tuttavia, poiché GPRMs vengono usati anche per archiviare i comandi del disco, la modifica dei valori usando [**SetGPRM**](setgprm-method.md) può causare un comportamento imprevedibile.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



