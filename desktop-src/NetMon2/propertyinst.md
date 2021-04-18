---
description: La struttura PROPERTYINST definisce un'istanza di una proprietà in un elemento di dati riconosciuti. Network Monitor alloca e compila una struttura PROPERTYINST quando una proprietà è associata all'acquisizione.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Struttura PROPERTYINST (Netmon. h)
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
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310961"
---
# <a name="propertyinst-structure"></a>Struttura PROPERTYINST

La struttura **PROPERTYINST** definisce un'istanza di una proprietà in un elemento di dati riconosciuti. Network Monitor alloca e compila una struttura **PROPERTYINST** quando una proprietà è associata all'acquisizione.

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

Puntatore alla struttura [PROPERTYINFO](propertyinfo.md) che definisce la proprietà.

</dd> <dt>

**szPropertyText**
</dt> <dd>

Puntatore a una stringa visualizzata nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.

</dd> <dt>

**lpData**
</dt> <dd>

Puntatore all'inizio dei dati per la proprietà. Il parser determina la posizione in cui vengono avviati i dati della proprietà.

</dd> <dt>

**lpByte**
</dt> <dd>

Puntatore ai dati **byte** .

</dd> <dt>

**lpWord**
</dt> <dd>

Puntatore ai dati di **Word** .

</dd> <dt>

**lpDword**
</dt> <dd>

Puntatore ai dati **DWORD** .

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Puntatore ai dati [**largeInt**](largeint.md) .

</dd> <dt>

**lpSysTime**
</dt> <dd>

Puntatore ai dati di [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> <dt>

**lpPropertyInstEx**
</dt> <dd>

Puntatore a una struttura [PROPERTYINSTEX](propertyinstex.md) . Il membro **lpPropertyInstEx** viene usato solo quando si chiama [AttachPropertyInstanceEx](attachpropertyinstanceex.md).

Se si usa **lpPropertyInstEx** , è necessario impostare il membro **DataLength** su 0xffff.

</dd> <dt>

**DataLength**
</dt> <dd>

Lunghezza dei dati per questa istanza della proprietà. Se il membro **lpPropertyInstEx** punta a una struttura [**PROPERTYINSTEX**](propertyinstex.md) , è necessario impostare **DataLength** su 0xffff.

</dd> <dt>

**Level**
</dt> <dd>

Informazioni sul livello.

</dd> <dt>

**HelpID**
</dt> <dd>

Identificatore del contesto del file della guida.

</dd> <dt>

**IFlags**
</dt> <dd>

Flag di condizione di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **PROPERTYINST** definisce un'istanza di una proprietà associata. Il parser accede alla struttura **PROPERTYINST** tramite varie funzioni helper. Ad esempio, quando viene chiamata la funzione [**FormatPropertyInstance**](formatpropertyinstance.md) per formattare i dati di una proprietà, viene modificato il membro **SzPropertyText** della struttura **PROPERTYINST** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> </dl>

 

