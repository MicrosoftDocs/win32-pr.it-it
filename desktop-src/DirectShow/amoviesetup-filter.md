---
description: La struttura AMOVIESETUP \_ FILTER contiene informazioni per la registrazione di un filtro.
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: AMOVIESETUP_FILTER struttura (Combase.h)
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
ms.openlocfilehash: fe50295f87e2932d3eb0fe53aac4896343a31441f8fa832bbaa69d5256846414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824791"
---
# <a name="amoviesetup_filter-structure"></a>Struttura AMOVIESETUP \_ FILTER

La **struttura AMOVIESETUP \_ FILTER** contiene informazioni per la registrazione di un filtro.

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

**Clsid**
</dt> <dd>

Identificatore di classe del filtro.

</dd> <dt>

**strName**
</dt> <dd>

Nome del filtro.

</dd> <dt>

**dwMerit**
</dt> <dd>

Filtrare il merito. Usato [**dall'interfaccia IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) durante la costruzione di un grafo di filtro. Per un elenco dei valori di merito, vedere [Merito](merit.md).

</dd> <dt>

**nPins**
</dt> <dd>

Numero di elementi nella matrice *lpPin.* Se *lpPin* è **NULL,** impostare questo membro su zero.

</dd> <dt>

**lpPin**
</dt> <dd>

Puntatore a una matrice di [**strutture \_ PIN AMOVIESETUP**](amoviesetup-pin.md) di dimensioni *nPins*. Ogni membro di questa matrice descrive un segnaposto sul filtro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per informazioni sull'uso di questa struttura, vedere [Come registrare DirectShow filtri](how-to-register-directshow-filters.md). Usare questa struttura solo per i filtri registrati nella categoria di filtro predefinita (CLSID \_ LegacyAmFilterCategory). Per registrare un filtro in una categoria diversa, usare il [**metodo IFilterMapper2::RegisterFilter,**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) come descritto in [Implementazione di DllRegisterServer](implementing-dllregisterserver.md).

> [!Note]  
> Il file di intestazione combase.h viene fornito con le classi [DirectShow base .](directshow-base-classes.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Strutture](directshow-structures.md)
</dt> </dl>

 

 




