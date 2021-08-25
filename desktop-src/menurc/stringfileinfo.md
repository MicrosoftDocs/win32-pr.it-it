---
title: Struttura StringFileInfo
description: Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene informazioni sulla versione che possono essere visualizzate per un linguaggio e una tabella codici specifici.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Struttura StringFileInfo Menu e altre risorse
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e130090c7281f6ef61ed0a3a82b822863bb5c12ff1194e26b07a70467db82cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720831"
---
# <a name="stringfileinfo-structure"></a>Struttura StringFileInfo

Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene informazioni sulla versione che possono essere visualizzate per un linguaggio e una tabella codici specifici.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Lunghezza, in byte, dell'intero **blocco StringFileInfo,** incluse tutte le strutture indicate dal **membro Children.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Questo membro è sempre uguale a zero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo di dati nella risorsa versione. Questo membro è 1 se la risorsa versione contiene dati di testo e 0 se la risorsa versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Stringa Unicode L"StringFileInfo".

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Il numero di zero parole necessario per allineare il **membro Children** su un limite a 32 bit.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **StringTable**](stringtable.md)**

</dd> <dd>

Matrice di una o più [**strutture StringTable.**](stringtable.md) Il **membro szKey** di ogni struttura **StringTable** indica la lingua e la tabella codici appropriate per la visualizzazione del testo in **tale struttura StringTable.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura in linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa versione e non viene visualizzata in nessuno dei file di intestazione forniti con Windows Software Development Kit (SDK).

Il **membro Children** della struttura VS [**\_ VERSIONINFO**](vs-versioninfo.md) può contenere zero o più **strutture StringFileInfo.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Stringtable**](stringtable.md)
</dt> <dt>

[**Stringa**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





