---
description: La \_ struttura del filtro AMOVIESETUP contiene informazioni per la registrazione di un filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Struttura AMOVIESETUP_FILTER (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331709"
---
# <a name="amoviesetup_filter-structure"></a>\_Struttura del filtro AMOVIESETUP

La struttura del **\_ filtro AMOVIESETUP** contiene informazioni per la registrazione di un filtro.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a>Members

<dl> <dt>

**clsID**
</dt> <dd>

Identificatore di classe del filtro.

</dd> <dt>

**strName**
</dt> <dd>

Nome del filtro.

</dd> <dt>

**dwMerit**
</dt> <dd>

Valore del filtro. Utilizzato dall'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) quando si crea un grafico di filtro. Per un elenco di valori di Merit, vedere [Merit](merit.md).

</dd> <dt>

**nPins**
</dt> <dd>

Numero di elementi nella matrice *lpPin* . Se *lpPin* è **null**, impostare questo membro su zero.

</dd> <dt>

**lpPin**
</dt> <dd>

Puntatore a una matrice di strutture [**AMOVIESETUP \_ pin**](amoviesetup-pin.md) di dimensioni *nPins*. Ogni membro di questa matrice descrive un pin sul filtro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per informazioni sull'uso di questa struttura, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md). Utilizzare questa struttura solo per i filtri registrati nella categoria di filtro predefinita (CLSID \_ LegacyAmFilterCategory). Per registrare un filtro in una categoria diversa, usare il metodo [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , come descritto in [implementazione di DllRegisterServer](implementing-dllregisterserver.md).

> [!Note]  
> Il file di intestazione ComBase. h viene fornito con le [classi base di DirectShow](directshow-base-classes.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DirectShow](directshow-structures.md)
</dt> </dl>

 

 




