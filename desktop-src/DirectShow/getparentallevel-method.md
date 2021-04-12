---
description: Il metodo DVDAdm. GetParentalLevel Recupera il livello padre che è stato salvato per ultimo nel registro di sistema.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Metodo GetParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401077"
---
# <a name="getparentallevel-method"></a>Metodo GetParentalLevel

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.GetParentalLevel` metodo recupera il livello padre che è stato salvato per ultimo nel registro di sistema.

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a>Valore restituito

Restituisce un numero intero compreso tra 1 e 8 che indica il livello padre predefinito.

## <a name="remarks"></a>Commenti

Il livello padre recuperato da questo metodo non è necessariamente lo stesso livello attualmente archiviato nel controllo MSWebDVD. per ottenere il livello attualmente archiviato nel controllo, chiamare il metodo [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) . Il valore-1 indica che la gestione padre è disabilitata.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



