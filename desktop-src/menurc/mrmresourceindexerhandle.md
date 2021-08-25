---
title: Struttura MrmResourceIndexerHandle (MrmResourceIndexer.h)
description: Rappresenta un handle opaco per un oggetto indicizzatore di risorse. L'handle è gestito dal sistema operativo. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti (PRI) e sistemi di compilazione personalizzati.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Menu della struttura MrmResourceIndexerHandle e altre risorse
- Puntatore alla struttura PMrmResourceIndexerHandle Menu e altre risorse
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c9cd18d6c828d5f9b5187f866d8ab637dfd4d58c3da0a8569bd8c910c7e872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825691"
---
# <a name="mrmresourceindexerhandle-structure"></a>Struttura MrmResourceIndexerHandle

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Rappresenta un handle opaco per un oggetto indicizzatore di risorse. L'handle è gestito dal sistema operativo. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a>Members

<dl> <dt>

**Gestire**
</dt> <dd>

Tipo: **PVOID**

</dd> <dd>

Handle opaco per un oggetto indicizzatore di risorse.

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

 

