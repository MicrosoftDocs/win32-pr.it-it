---
title: Struttura VarFileInfo
description: Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene informazioni sulla versione che non dipendono da una particolare combinazione di linguaggio e tabella codici.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Struttura VarFileInfo Menu e altre risorse
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddae8f913e199e0a1219e5ec36012ba3a3eaf24708ca6771ec075b497107418e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733392"
---
# <a name="varfileinfo-structure"></a>Struttura VarFileInfo

Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene informazioni sulla versione che non dipendono da una particolare combinazione di linguaggio e tabella codici.

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

Tipo: **WORD**

</dd> <dd>

Lunghezza, in byte, dell'intero blocco **VarFileInfo,** incluse tutte le strutture indicate dal **membro Children.**

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

Tipo di dati nella risorsa della versione. Questo membro è 1 se la risorsa versione contiene dati di testo e 0 se la risorsa versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Stringa Unicode L"VarFileInfo".

</dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Il numero di zero parole necessario per allineare il **membro Children** su un limite a 32 bit.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **Var**](var-str.md)**

</dd> <dd>

Contiene in genere un elenco di lingue supportate dall'applicazione o dalla DLL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura in linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa versione e non viene visualizzata in nessuno dei file di intestazione forniti con Windows Software Development Kit (SDK).

Il **membro Children** della struttura VS [**\_ VERSIONINFO**](vs-versioninfo.md) può contenere zero o una **struttura VarFileInfo.**

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

 

 





