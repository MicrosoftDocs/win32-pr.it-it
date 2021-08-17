---
description: La struttura CAPTUREFILTER contiene i dati del filtro di acquisizione.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Struttura CAPTUREFILTER (Netmon.h)
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
ms.openlocfilehash: de5ab95ab395d50afb41223a458342706da1df7434d524f21c230436b3b9c7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796361"
---
# <a name="capturefilter-structure"></a>Struttura CAPTUREFILTER

La **struttura CAPTUREFILTER** contiene i dati del filtro di acquisizione.

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
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**CAPTUREFILTER \_ I \_ FLAG INCLUDONO TUTTI I 0X0001 \_ \_ SAPS**</dt> <dt></dt> </dl>       | Include tutti i criteri di accesso condiviso come frame accettabili.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**CAPTUREFILTER \_ I \_ FLAG INCLUDONO TUTTI I TIPI \_ \_ 0X0002**</dt> <dt></dt> </dl> | Includere tutti i tipi di dati come frame accettabili.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**CAPTUREFILTER \_ FLAG \_ SOLO \_ LOCALI**</dt> <dt>0X0008</dt> </dl>                          | Nessuna modalità P<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**CAPTUREFILTER \_ I FLAG \_ \_ MANTENGONO LE**</dt> <dt>0X0020</dt> </dl>                                | Mantenere i frame MAC SMT e Token Ring.<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

Puntatore a una matrice di valori SAP. Questo membro indica i valori SAP validi da passare al driver. Se captureFILTER FLAGS INCLUDE ALL SAPS è impostato, questo diventa un elenco di eccezioni \_ \_ \_ \_ (includere tutti i SAPS tranne questi).

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Puntatore a una matrice di valori Etype. Indica i valori Etype validi da passare al driver. Se captureFILTER FLAGS INCLUDE ALL ETYPES è impostato, questo diventa un elenco di eccezioni \_ \_ \_ \_ (includere tutti i tipi tranne questi).

</dd> <dt>

**nSaps**
</dt> <dd>

Numero di sap nella tabella SAP.

</dd> <dt>

**nEtypes**
</dt> <dd>

Numero di Etype nella tabella Etype.

</dd> <dt>

**AddressTable**
</dt> <dd>

Nome della tabella di indirizzi.

</dd> <dt>

**Filterexpression**
</dt> <dd>

Struttura EXPRESSION. Contiene la parte relativa alle corrispondenze dei criteri del filtro di acquisizione.

</dd> <dt>

**Trigger**
</dt> <dd>

Riservato.

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

Se questo membro non è 0, specifica il numero di byte da mantenere per ogni frame ricevuto. Se è 0, mantenere l'intero frame.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

La combinazione di flag, valori ed espressioni determina quali frame verranno passati dal driver che utilizza i dati della struttura. Per altre informazioni sull'implementazione di **una struttura CAPTUREFILTER,** vedere [Capture Filters](capture-filters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TABELLA INDIRIZZI](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[Espressione](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




