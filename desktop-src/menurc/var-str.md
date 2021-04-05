---
title: Struttura var
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene in genere un elenco di coppie di identificatori di tabella codici e lingue supportate dalla versione dell'applicazione o dalla DLL.
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
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874526"
---
# <a name="var-structure"></a>Struttura var

Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene in genere un elenco di coppie di identificatori di tabella codici e lingue supportate dalla versione dell'applicazione o dalla DLL.

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

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, della struttura **var** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, del membro del **valore** .

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tipo di dati nella risorsa della versione. Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Stringa Unicode L "Translation".

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Il numero di parole necessarie per allineare il membro del **valore** a un limite di 32 bit è pari a zero.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Matrice di uno o più valori che sono coppie di identificatori della tabella codici e della lingua. Per ulteriori informazioni, vedere la sezione Osservazioni seguente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).

Se si usa la struttura **var** per elencare le lingue supportate dall'applicazione o dalla dll invece di usare più risorse della versione, usare il membro **valore** per contenere una matrice di valori **DWORD** che indica le combinazioni di lingua e tabella codici supportate da questo file. La parola più bassa di ogni **valore DWORD** deve contenere un identificatore di lingua Microsoft e la parola più significativa deve contenere il numero della tabella codici IBM. La parola di ordine superiore o inferiore può essere zero, a indicare che il file è indipendente dalla lingua o dalla tabella codici. Se la struttura **var** viene omessa, il file verrà interpretato sia come lingua sia come tabella codici indipendente.

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

[**Un'STRINGTABLE**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





