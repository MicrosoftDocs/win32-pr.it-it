---
description: La struttura MXDC dell' \_ \_ intestazione \_ di escape T include il codice operativo per una chiamata a ExtEscape con MXDC \_ escape come parametro nEscape. Fornisce anche le dimensioni dei buffer di input e di output.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Struttura MXDC_ESCAPE_HEADER_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885173"
---
# <a name="mxdc_escape_header_t-structure"></a>\_ \_ Struttura T dell'intestazione di escape MXDC \_

La struttura **MXDC dell' \_ intestazione di escape \_ \_ T** include il codice operativo per una chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ escape**](mxdc-escape.md) come parametro *nEscape* . Fornisce anche le dimensioni dei buffer di input e di output.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a>Members

<dl> <dt>

**cbInput**
</dt> <dd>

Dimensioni del buffer di input che verranno passate al parametro *lpszOutData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**cbOutput**
</dt> <dd>

Dimensione del buffer di output. Si tratta dello stesso valore del parametro *cbOutput* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**Codice operativo**
</dt> <dd>

Costante del codice che indica a MXDC cosa fare.



| Codice operativo                      | Descrizione                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ ottenere il \_ nome file                | Restituisce, nel parametro *lpszOutData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , il percorso completo del file di output come stringa con terminazione zero o la dimensione di tale stringa. Vedere la sezione Osservazioni.                   |
| MXDCOP \_ \_ documento fisso di PRINTTICKET \_ \_ | Associa un ticket di stampa a una sequenza di documenti fissa XPS.                                                                                                                                                         |
| \_ \_ doc fisso PRINTTICKET \_ MXDCOP      | Associa un ticket di stampa a un documento XPS.                                                                                                                                                                        |
| \_ \_ pagina fissa PRINTTICKET \_ MXDCOP     | Associa un ticket di stampa a una pagina XPS.                                                                                                                                                                            |
| MXDCOP \_ set \_ S0PAGE                  | Invia il markup XPS della pagina corrente all'output.                                                                                                                                                                |
| MXDCOP \_ impostare \_ la \_ risorsa S0PAGE        | Invia all'output una risorsa nella pagina, ad esempio un'immagine o un tipo di carattere.                                                                                                                                                 |
| MXDCOP \_ impostare \_ la \_ modalità XPSPASSTHRU       | Inserisce il MXDC in uno stato pass-through, consentendo a un'applicazione di scrivere XPS direttamente nel file di output senza alcuna elaborazione da parte di MXDC. In questo modo è possibile scrivere un intero documento o persino una sequenza di documenti. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Prima di chiamare [**MXDC \_ escape**](mxdc-escape.md), le \_ applicazioni devono prima verificare che il driver sia MXDC chiamando [**EXTESCAPE**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con l'escape [**GetTechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Se il driver è MXDC, la funzione restituisce la stringa con terminazione zero " http://schemas.microsoft.com/xps/2005/06 ".

Questa struttura è sempre all'inizio dei dati passati alla funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) nel parametro *lpszInData* .

Quando **OpCode** è MXDCOP \_ get \_ FileName:

-   Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito solo dall' **\_ \_ intestazione \_ T di escape MXDC** .
-   Ottenere il nome del file di output chiamando [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) due volte.
    1.  La prima volta, passare 4 al parametro *cbOutput* di [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Impostare il parametro *lpszOutData* in modo che punti a tutti i 4 byte allocati di memoria. La dimensione del percorso completo del file verrà restituita nel parametro *lpszOutData* di **ExtEscape**.
    2.  Chiamare quindi di nuovo la funzione. Questa volta imposta sia *cbOutput* che *cbInput* su 4 + *DataSize*. Il percorso completo del file verrà restituito in una struttura [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .

Quando **OpCode** è MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq o MXDCOP \_ PrintTicket \_ fixed \_ doc:

-   Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenata in una struttura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e una chiamata a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

Quando **OpCode** è MXDCOP \_ PRINTTICKET \_ fixed \_ Page:

-   Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenata in una struttura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Quando **OpCode** è MXDCOP \_ set \_ S0PAGE:

-   Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenata in una struttura [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).
-   L'applicazione chiamante è responsabile della convalida del codice XML.
-   Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ impostare \_ \_ la risorsa S0PAGE come **OpCode** per ogni risorsa nella pagina prima di chiamarla con MXDCOP \_ set \_ S0PAGE.

Quando **OpCode** è MXDCOP \_ set \_ S0PAGE \_ Resource:

-   Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenata in una struttura [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), ma possono essere presenti più chiamate tra le chiamate a **Startpage** e **EndPage** .
-   Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ impostare \_ \_ la risorsa S0PAGE come **OpCode** per ogni risorsa nella pagina prima di chiamarla con MXDCOP \_ set \_ S0PAGE.

Quando **OpCode** è MXDCOP \_ set \_ XPSPASSTHRU \_ mode:

-   Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito solo dall' **\_ \_ intestazione \_ T di escape MXDC** .
-   Questa chiamata deve essere eseguita prima della chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>MXDC. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**\_escape MXDC**](mxdc-escape.md)
</dt> </dl>

 

