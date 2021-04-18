---
description: La struttura CAPTUREFILTER contiene i dati del filtro di acquisizione.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Struttura CAPTUREFILTER (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314185"
---
# <a name="capturefilter-structure"></a>Struttura CAPTUREFILTER

La struttura **capturefilter** contiene i dati del filtro di acquisizione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a>Members

<dl> <dt>

**FilterFlags**
</dt> <dd>

Flag che descrivono il contenuto del filtro di acquisizione.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**Capturefilter \_ \_I flag includono \_ tutti i \_ succhi**</dt> <dt>0x0001</dt> </dl>       | Include tutti i succhi come frame accettabili.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**Capturefilter \_ \_I flag includono \_ tutti \_ etype del**</dt> <dt>0x0002</dt> </dl> | Includere tutti i ETYPE del come frame accettabili.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**Capturefilter \_ CONTRASSEGNA \_ \_ solo**</dt> <dt>0x0008</dt> locali </dl>                          | Nessuna modalità P<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**Capturefilter \_ FLAG \_ Keep \_**</dt> <dt>0x0020</dt> RAW </dl>                                | Mantieni i frame MAC SMT e token ring.<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

Puntatore a una matrice di valori SAP. Questo membro indica i valori SAP validi da passare al driver. Se \_ i flag capturefilter \_ includono \_ tutti i \_ succhi sono impostati, questo diventa un elenco di eccezioni (includere tutti i succhi ad eccezione di questi).

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Puntatore a una matrice di valori etype. Ciò indica i valori ETYPE validi da passare al driver. Se \_ i flag capturefilter \_ includono \_ tutti i \_ etype del impostati, questo diventa un elenco di eccezioni (includere tutti i ETYPE del ad eccezione di questi).

</dd> <dt>

**nSaps**
</dt> <dd>

Numero di succhi nella tabella SAP.

</dd> <dt>

**nEtypes**
</dt> <dd>

Numero di ETYPE del nella tabella etype.

</dd> <dt>

**AddressTable**
</dt> <dd>

Nome della tabella degli indirizzi.

</dd> <dt>

**FilterExpression**
</dt> <dd>

Struttura dell'espressione. Contiene la parte relativa alla corrispondenza dei criteri del filtro di acquisizione.

</dd> <dt>

**Trigger**
</dt> <dd>

Riservato.

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

Se il membro non è 0, specifica il numero di byte da memorizzare per ogni frame ricevuto. Se è 0, Mantieni l'intero frame.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

La combinazione di flag, valori ed espressioni determina quali frame verranno passati dal driver che utilizza i dati della struttura. Per ulteriori informazioni sull'implementazione di una struttura **capturefilter** , vedere [Capture filters](capture-filters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ADDRESSTABLE](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[ESPRESSIONE](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




