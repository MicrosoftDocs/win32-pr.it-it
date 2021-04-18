---
title: Struttura VarFileInfo
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla versione che non dipendono da una determinata combinazione di lingua e tabella codici.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menu struttura VarFileInfo e altre risorse
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302206"
---
# <a name="varfileinfo-structure"></a>Struttura VarFileInfo

Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene informazioni sulla versione che non dipendono da una determinata combinazione di lingua e tabella codici.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, dell'intero blocco **VarFileInfo** , incluse tutte le strutture indicate dal membro **figlio** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Questo membro è sempre uguale a zero.

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

Stringa Unicode L "VarFileInfo".

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **var**](var-str.md)**

</dd> <dd>

Contiene in genere un elenco di lingue supportate dall'applicazione o dalla DLL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).

Il membro **figlio** della struttura di [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) può contenere zero o una o più strutture **VarFileInfo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





