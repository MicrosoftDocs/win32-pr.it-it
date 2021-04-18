---
title: Struttura STOWED_EXCEPTION_INFORMATION_V2
description: Contiene informazioni sulle eccezioni riposte.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- Struttura STOWED_EXCEPTION_INFORMATION_V2 Segnalazione errori Windows
- Puntatore alla struttura PSTOWED_EXCEPTION_INFORMATION_V2 Segnalazione errori Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302378"
---
# <a name="stowed_exception_information_v2-structure"></a>\_Struttura di informazioni sulle eccezioni riportate \_ \_ v2

Contiene informazioni sulle eccezioni riposte.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a>Members

<dl> <dt>

**Intestazione**
</dt> <dd>

Tipo: **[ **\_ \_ \_ intestazione informazioni eccezione** riposte](stowed-exception-information-header.md)**

</dd> <dd>

Struttura [**dell' \_ \_ \_ intestazione delle informazioni sull'eccezione**](stowed-exception-information-header.md) riposta che contiene informazioni per la struttura padre.

</dd> <dt>

**ResultCode**
</dt> <dd>

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Codice [**HRESULT**](/windows/desktop/WinProg/windows-data-types) per l'eccezione riposta.

</dd> <dt>

**ExceptionForm**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore a 2 bit che identifica il formato dell'eccezione.



| Valore                                                                                                                                                                                                                                                                  | Significato                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> Ricollocato <dt>**\_ Formato di eccezione 0x01 \_ \_ binario**</dt> <dt></dt> </dl> | Questo valore indica che il formato dell'eccezione è binario.<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> Ricollocato <dt>**\_ Formato dell'eccezione \_ \_ testo**</dt> <dt>0x02</dt> </dl>       | Questo valore indica che il formato dell'eccezione è testo.<br/>   |



 

</dd> <dt>

**ThreadId**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore A 30 bit che identifica il thread che ha generato l'eccezione. Il valore viene spostato a destra di 2 bit quando viene archiviato. Per convertirlo di nuovo in un ID di thread valido, spostare il valore a sinistra di 2. Ad esempio:

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

(*struct senza nome*)
</dt> <dd>

I membri di questa struttura nidificata sono validi solo se il membro **ExceptionForm** è impostato **su \_ \_ \_ binary form Exception**.

<dl> <dt>

**ExceptionAddress**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntatore che contiene l'indirizzo dell'eccezione.

</dd> <dt>

**StackTraceWordSize**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Dimensione, in byte, di ogni parola nell'analisi dello stack a cui fa riferimento il membro **StackTrace** . Questo valore è impostato su 4 per le piattaforme a 32 bit e 8 per le piattaforme a 64 bit.

</dd> <dt>

**StackTraceWords**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di parole nell'analisi dello stack a cui punta il membro **StackTrace** . Il numero di parole è uguale al numero di elementi nella matrice.

</dd> <dt>

**StackTrace**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntatore a un blocco di memoria che contiene l'analisi dello stack.

</dd> </dl> </dd> <dt>

(*struct senza nome*)
</dt> <dd>

Il membro di questa struttura annidata è valido solo se il membro **ExceptionForm** è impostato per il **testo del \_ \_ form \_ dell'eccezione**.

<dl> <dt>

**ErrorText**
</dt> <dd>

Tipo: **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntatore a una stringa con terminazione null che contiene il testo dell'errore dell'eccezione.

</dd> </dl> </dd> <dt>

**NestedExceptionType**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valore a 32 bit che specifica il tipo di oggetto a cui fa riferimento il membro **annidato** . Definire il valore con questa macro di definizione del tipo di scambio di byte che presuppone little-endian:

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

Di seguito sono riportate alcune definizioni di tipi comuni:



| Valore                                                                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> Ricollocato <dt>**\_ \_Tipo annidato eccezione \_ \_ None**</dt> <dt>(0x00000000)</dt> </dl>                                  | Questo valore specifica che non è presente alcun oggetto eccezione annidato.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> Ricollocato <dt>**\_ Tipo \_ \_ \_**</dt> annidato eccezione tipo annidato Win32 <dt> \_ \_ \_ (' W32E ')</dt> </dl>    | Questo valore specifica che il membro **annidato** fa riferimento a un oggetto [**\_ record di eccezione**](/windows/desktop/api/winnt/ns-winnt-exception_record) .<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> Ricollocato <dt>**\_ tipo \_ \_ \_**</dt> annidato dell'eccezione ristivato del tipo annidato <dt> \_ \_ \_ (' Stow ')</dt> </dl> | Questo valore specifica che il membro **annidato** fa riferimento a un altro oggetto eccezione stivata. L'altro oggetto eccezione riposta può essere un oggetto di **\_ \_ informazioni sulle \_ eccezioni** stivate o una versione diversa con un membro di **intestazione** valido, ovvero un membro di **intestazione** che contiene un' [**\_ \_ \_ intestazione di informazioni sull'eccezione**](stowed-exception-information-header.md)riposta valida.<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> Ricollocato <dt>**\_ Tipo annidato eccezione \_ \_ \_ CLR**</dt> <dt>ristivato tipo annidato \_ \_ \_ (' nel clr1')</dt> </dl>          | Questo valore specifica che il membro **annidato** fa riferimento a un oggetto eccezione ' nel clr1'.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> Ricollocato <dt>**\_ Tipo \_ \_ \_**</dt> annidato eccezione tipo annidato eccezione Leo <dt>stivato \_ \_ \_ (' Leo1')</dt> </dl>          | Questo valore specifica che il membro **annidato** fa riferimento a un oggetto eccezione della lingua.<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**Annidaexception**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntatore a un tipo di eccezione annidato. Il tipo di oggetto è indicato dal membro **NestedExceptionType** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Ricollocato **\_ \_Le informazioni sull'eccezione \_ v2** e l' [**\_ \_ \_ intestazione delle informazioni sulle eccezioni**](stowed-exception-information-header.md) riposte non sono attualmente definite in un'intestazione disponibile pubblicamente, pertanto è necessario definirle nel codice sorgente prima di utilizzarle.

La struttura di **\_ \_ informazioni \_ sull'eccezione ristivata** è identica a questa struttura, ad eccezione del fatto che non contiene i membri **NestedExceptionType** e **annidaexception** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                         |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RECORD di eccezione \_**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**\_ \_ intestazione informazioni sulle eccezioni riposte \_**](stowed-exception-information-header.md)
</dt> </dl>

 

