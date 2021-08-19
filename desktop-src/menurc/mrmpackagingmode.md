---
title: Enumerazione MrmPackagingMode (MrmResourceIndexer.h)
description: Definisce costanti che specificano il tipo di file PRI che devono essere creati da MrmCreateResourceFile e MrmCreateResourceFileInMemory.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Menu e altre risorse dell'enumerazione MrmPackagingMode
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b4e968a43ba08786cc433b199bef5c07431420ac5942646530960279ea853e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870150"
---
# <a name="mrmpackagingmode-enumeration"></a>Enumerazione MrmPackagingMode

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Definisce costanti che specificano il tipo di file PRI che devono essere creati da [**MrmCreateResourceFile**](mrmcreateresourcefile.md) e [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md). Per altre informazioni e procedure dettagliate basate su scenario su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti e sistemi [di compilazione personalizzati.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**
</dt> <dd>

Specifica che deve essere creato un singolo file PRI.

</dd> <dt>

<span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**
</dt> <dd>

Specifica che devono essere creati più file PRI. viene suddiviso automaticamente in base a tutti i qualificatori supportati (in particolare, lingua e scalabilità).

</dd> <dt>

<span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**
</dt> <dd>

Specifica che deve essere creato un file PRI satellite del componente aggiuntivo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1803 \[\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo \[ app desktop server\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

