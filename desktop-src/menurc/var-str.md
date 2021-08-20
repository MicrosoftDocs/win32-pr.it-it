---
title: Struttura Var
description: Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene in genere un elenco di coppie di identificatori di lingua e tabella codici supportati dalla versione dell'applicazione o della DLL.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menu struttura var e altre risorse
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48537009b56d2b37f4508871049463a65a12965c31658e932716832955503f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599581"
---
# <a name="var-structure"></a>Struttura Var

Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene in genere un elenco di coppie di identificatori di lingua e tabella codici supportati dalla versione dell'applicazione o della DLL.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Lunghezza, in byte, della **struttura Var.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Lunghezza, in byte, del **membro** Value.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo di dati nella risorsa della versione. Questo membro è 1 se la risorsa versione contiene dati di testo e 0 se la risorsa versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Stringa Unicode L"Translation".

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Il numero di zero parole necessario per allineare il **membro Value** su un limite a 32 bit.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Matrice di uno o più valori che sono coppie di identificatori di lingua e tabella codici. Per altre informazioni, vedere la sezione Osservazioni seguente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura in linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa versione e non viene visualizzata in nessuno dei file di intestazione forniti con Windows Software Development Kit (SDK).

Se si usa la struttura **Var** per elencare le lingue supportate dall'applicazione o dalla DLL invece di usare più risorse di versione, usare il membro **Value** per contenere una matrice di valori **DWORD** che indica le combinazioni di linguaggio e tabella codici supportate da questo file. La parola più bassa di ogni **DWORD** deve contenere un identificatore di lingua Microsoft e la parola di ordine superiore deve contenere il numero della tabella codici IBM. La parola più importante o meno importante può essere zero, a indicare che il file è indipendente dalla lingua o dalla tabella codici. Se la **struttura Var** viene omessa, il file verrà interpretato come indipendente dal linguaggio e dalla tabella codici.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Stringtable**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





