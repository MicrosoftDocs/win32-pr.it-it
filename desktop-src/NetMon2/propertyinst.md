---
description: La struttura PROPERTYINST definisce un'istanza di una proprietà in una parte di dati riconosciuti. Network Monitor alloca e compila una struttura PROPERTYINST quando una proprietà è associata all'acquisizione.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Struttura PROPERTYINST (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0d1c338fb8b4e63f03bff422e25578132476f70d932e8f17d5b0c39a0f6416e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778501"
---
# <a name="propertyinst-structure"></a>Struttura PROPERTYINST

La **struttura PROPERTYINST** definisce un'istanza di una proprietà in una parte di dati riconosciuti. Network Monitor alloca e compila una **struttura PROPERTYINST** quando una proprietà è associata all'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a>Members

<dl> <dt>

**lpPropertyInfo**
</dt> <dd>

Puntatore alla [struttura PROPERTYINFO](propertyinfo.md) che definisce la proprietà.

</dd> <dt>

**szPropertyText**
</dt> <dd>

Puntatore a una stringa visualizzata nel riquadro dei dettagli dell'interfaccia Network Monitor interfaccia utente.

</dd> <dt>

**lpData**
</dt> <dd>

Puntatore all'inizio dei dati per la proprietà. Il parser determina la posizione di inizio dei dati della proprietà.

</dd> <dt>

**lpByte**
</dt> <dd>

Puntatore ai **dati BYTE.**

</dd> <dt>

**lpWord**
</dt> <dd>

Puntatore ai **dati WORD.**

</dd> <dt>

**lpDword**
</dt> <dd>

Puntatore ai **dati DWORD.**

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Puntatore ai [**dati LARGEINT.**](largeint.md)

</dd> <dt>

**lpSysTime**
</dt> <dd>

Puntatore ai [**dati SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

**lpPropertyInstEx**
</dt> <dd>

Puntatore a [una struttura PROPERTYINSTEX.](propertyinstex.md) Il **membro lpPropertyInstEx** viene usato solo quando si chiama [AttachPropertyInstanceEx](attachpropertyinstanceex.md).

Se **si usa lpPropertyInstEx,** è necessario impostare il membro **DataLength** su 0xFFFF.

</dd> <dt>

**Datalength**
</dt> <dd>

Lunghezza dei dati per questa istanza della proprietà . Se il **membro lpPropertyInstEx** punta a una [**struttura PROPERTYINSTEX,**](propertyinstex.md) è necessario impostare **DataLength** su 0xFFFF.

</dd> <dt>

**Level**
</dt> <dd>

Informazioni sul livello.

</dd> <dt>

**HelpID**
</dt> <dd>

Identificatore del contesto del file della Guida.

</dd> <dt>

**IFlags**
</dt> <dd>

Flag della condizione di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura PROPERTYINST** definisce un'istanza di una proprietà associata. Il parser accede alla **struttura PROPERTYINST** tramite diverse funzioni helper. Ad esempio, quando viene chiamata la funzione [**FormatPropertyInstance**](formatpropertyinstance.md) per formattare i dati di una proprietà, modifica il membro **szPropertyText** della **struttura PROPERTYINST.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> </dl>

 

