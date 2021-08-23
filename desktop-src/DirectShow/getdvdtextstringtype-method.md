---
description: Il metodo GetDVDTextStringType recupera un valore che indica il tipo di informazioni contenute nella stringa di testo DVD specificata.
ms.assetid: 8e22fa2e-e7eb-4dd8-b365-631986bad03e
title: Metodo GetDVDTextStringType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4ad7985101379dd37d605f830ee9b20b4138e8f4c96092aaeb0ae347261adbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812531"
---
# <a name="getdvdtextstringtype-method"></a>Metodo GetDVDTextStringType

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetDVDTextStringType` metodo recupera un valore che indica il tipo di informazioni contenute nella stringa di testo DVD specificata.

``` syntax
[ iStringType = ] MSWebDVD.GetDVDTextStringType(iLangIndex, iStringIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Specifica la lingua della stringa di testo come integer.

</dd> <dt>

<span id="iStringIndex"></span><span id="istringindex"></span><span id="ISTRINGINDEX"></span>*iStringIndex*
</dt> <dd>

Specifica il numero di indice della stringa di testo come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che indica il tipo di informazioni contenute nella stringa.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



