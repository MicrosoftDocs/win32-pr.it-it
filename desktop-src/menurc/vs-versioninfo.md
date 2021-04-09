---
title: Struttura VS_VERSIONINFO
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Si tratta della struttura radice che contiene tutte le altre strutture di informazioni sulla versione del file.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- Menu struttura VS_VERSIONINFO e altre risorse
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121426"
---
# <a name="vs_versioninfo-structure"></a>Struttura di VS \_ VERSIONINFO

Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Si tratta della struttura radice che contiene tutte le altre strutture di informazioni sulla versione del file.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, della struttura di **Visual Studio \_ VERSIONINFO** . Questa lunghezza non include alcun riempimento che allinea i dati delle risorse della versione successiva in un limite di 32 bit.

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, del membro del **valore** . Questo valore è zero se non è presente alcun membro di **valore** associato alla struttura della versione corrente.

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

Stringa Unicode L "informazioni sulla \_ versione di vs \_ ".

</dd> <dt>

**Padding1**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Contiene un numero di parole pari a zero, se necessario, per allineare il membro del **valore** a un limite di 32 bit.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **[ **vs \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**

</dd> <dd>

Dati arbitrari associati a questa struttura di **Visual Studio \_ VERSIONINFO** . Il membro **wValueLength** specifica la lunghezza di questo membro. Se **wValueLength** è zero, questo membro non esiste.

</dd> <dt>

**Padding2**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Il numero di parole necessarie per allineare il membro **figlio** al limite di 32 bit è pari a zero. Questi byte non sono inclusi in **wValueLength**. Questo membro è facoltativo.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Matrice di zero o una struttura [**StringFileInfo**](stringfileinfo.md) e zero o una struttura [**VarFileInfo**](varfileinfo.md) che sono elementi figlio della struttura corrente di **vs \_ VERSIONINFO** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





