---
description: Contiene informazioni che definiscono un nuovo elenco degli elementi usati più di recente. Usato da CreateMRUListW.
title: Struttura MRUINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840762"
---
# <a name="mruinfo-structure"></a>Struttura MRUINFO

Contiene informazioni che definiscono un nuovo elenco degli elementi usati più di recente. Usato da [**CreateMRUListW.**](createmrulist.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensione della struttura .

</dd> <dt>

**Umax**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Numero massimo di voci nell'elenco MRU.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Uno o più dei flag seguenti.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARY** (0x0001)


</dt> <dd>

I dati vengono archiviati nel Registro di sistema come dati binari anziché come dati stringa.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)


</dt> <dd>

Scrivere le modifiche alla versione dell'elenco MRU archiviata nel Registro di sistema solo quando viene aggiunto un nuovo elemento o le risorse dell'elenco MRU vengono liberate dalla memoria. Si noti che la versione attiva dell'elenco MRU in memoria viene aggiornata immediatamente in risposta a qualsiasi modifica nel contenuto o nell'ordinamento.

</dd> </dl> </dd> <dt>

**Hkey**
</dt> <dd>

Tipo: **HKEY**

</dd> <dd>

Handle per la chiave attualmente aperta o uno dei valori predefiniti seguenti in cui archiviare i dati MRU.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**HKEY \_ CURRENT \_ USER**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**HKEY \_ LOCAL \_ MACHINE**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

Tipo: **LPCTSTR**

</dd> <dd>

Sottochiave in cui archiviare i dati MRU.

</dd> <dt>

**lpfnCompare**
</dt> <dd>

Tipo: **[ **MRUCMPPROC**](mrucmpproc.md)**

</dd> <dd>

Puntatore a una funzione di confronto dei dati facoltativa che può essere usata per determinare se un elemento è presente nell'elenco MRU. Ciò è utile quando l'elenco MRU è stato creato con il flag **MRU \_ BINARY.** Se questo membro è **NULL,** vengono usate le funzioni standard di confronto tra stringhe. Per i dati binari, viene usato un confronto diretto della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è definita in un file di intestazione. È necessario definirlo manualmente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |
| Nomi Unicode e ANSI<br/>   | **MRUINFOW** (Unicode) e **MRUINFOA** (ANSI)<br/>  |



 

 




