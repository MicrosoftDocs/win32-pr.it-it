---
description: La struttura MXDC ESCAPE HEADER T contiene il codice dell'operazione per una chiamata \_ \_ a \_ ExtEscape con MXDC \_ ESCAPE come parametro nEscape. Fornisce anche le dimensioni dei buffer di input e di output.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: MXDC_ESCAPE_HEADER_T struttura (Mxdc.h)
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
ms.openlocfilehash: 53dd83e362ab21938121a986ee2402076d72f870460bc9db608b9a048cee0f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099075"
---
# <a name="mxdc_escape_header_t-structure"></a>Struttura MXDC \_ ESCAPE \_ HEADER \_ T

La **struttura MXDC \_ ESCAPE HEADER \_ \_ T** contiene il codice dell'operazione per una chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ ESCAPE**](mxdc-escape.md) come *parametro nEscape.* Fornisce anche le dimensioni dei buffer di input e di output.

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

Dimensione del buffer di input che verrà passato al parametro *lpszOutData* della [**funzione ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)

</dd> <dt>

**cbOutput**
</dt> <dd>

Dimensione del buffer di output. Si tratta dello stesso valore del *parametro cbOutput* della funzione [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)

</dd> <dt>

**Opcode**
</dt> <dd>

Costante di codice che indica a MXDC cosa fare.



| Codice operativo                      | Descrizione                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ GET \_ FILENAME                | Restituisce, nel parametro *lpszOutData* della funzione [**ExtEscape,**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) il percorso completo del file di output come stringa con terminazione zero o le dimensioni di tale stringa. Vedere la sezione Osservazioni.                   |
| MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ | Associa un ticket di stampa a una sequenza di documenti xps fissa.                                                                                                                                                         |
| MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC      | Associa un ticket di stampa a un documento XPS.                                                                                                                                                                        |
| PAGINA FISSA DI MXDCOP \_ PRINTTICKET \_ \_     | Associa un ticket di stampa a una pagina XPS.                                                                                                                                                                            |
| MXDCOP \_ SET \_ S0PAGE                  | Invia il markup XPS della pagina corrente all'output.                                                                                                                                                                |
| MXDCOP \_ SET \_ S0PAGE \_ RESOURCE        | Invia una risorsa nella pagina, ad esempio un'immagine o un tipo di carattere, all'output.                                                                                                                                                 |
| MXDCOP \_ IMPOSTARE LA MODALITÀ \_ XPSPASSTHRU \_       | Inserisce MXDC in uno stato pass-through, consentendo a un'applicazione di scrivere XPS direttamente nel file di output senza alcuna elaborazione da parte di MXDC. In questo modo è possibile scrivere un intero documento o anche una sequenza di documenti. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Prima di [**chiamare MXDC \_ ESCAPE,**](mxdc-escape.md)le applicazioni devono prima verificare che il driver sia MXDC chiamando \_ [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con l'escape [**GETTECHNOLOGY.**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) Se il driver è MXDC, la funzione restituisce la stringa con terminazione zero " http://schemas.microsoft.com/xps/2005/06 ".

Questa struttura si trova sempre all'inizio dei dati passati alla funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) nel parametro *lpszInData.*

Quando **opCode è** MXDCOP \_ GET \_ FILENAME:

-   Il *parametro lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito solo dalla **struttura MXDC ESCAPE HEADER \_ \_ \_ T.**
-   Ottenere il nome file di output chiamando [**ExtEscape due**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) volte.
    1.  La prima volta, passare 4 al *parametro cbOutput* di [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Impostare il *parametro lpszOutData* in modo che punti a tutti i 4 byte di memoria allocati. Le dimensioni del percorso completo del file verranno restituite nel parametro *lpszOutData* di **ExtEscape**.
    2.  Chiamare quindi di nuovo la funzione . Questa volta impostare *sia cbOutput che* *cbInput* su 4+ *DataSize*. Il percorso completo del file verrà restituito in [**una struttura MxdcGetFileNameData.**](mxdcgetfilenamedata.md)

Quando **opCode è** MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ o MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC:

-   Il *parametro lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla struttura **MXDC ESCAPE HEADER \_ \_ \_ T** e da una struttura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenata in una struttura [**MxdcPrintTicketEscape.**](mxdcprintticketescape.md)
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve verificarsi tra una chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e una chiamata a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

Quando **opCode è** MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE:

-   Il *parametro lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla struttura **MXDC ESCAPE HEADER \_ \_ \_ T** e da una struttura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenata in una struttura [**MxdcPrintTicketEscape.**](mxdcprintticketescape.md)
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve verificarsi tra una chiamata a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Quando **opCode** è MXDCOP \_ SET \_ S0PAGE:

-   Il *parametro lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla struttura **MXDC ESCAPE HEADER \_ \_ \_ T** e da una struttura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenata in una struttura [**MxdcS0PagePassthroughEscape.**](mxdcs0pagepassthroughescape.md)
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve verificarsi tra una chiamata a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).
-   L'applicazione chiamante è responsabile della convalida del codice XML.
-   L'utilizzo dello streaming è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP SET S0PAGE RESOURCE come opCode per ogni risorsa nella pagina prima di chiamarla con \_ \_ \_ MXDCOP  \_ SET \_ S0PAGE.

Quando **opCode** è MXDCOP \_ SET \_ S0PAGE \_ RESOURCE:

-   Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla struttura **MXDC \_ ESCAPE HEADER \_ \_ T** e da una struttura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenata in una struttura [**MxdcS0PageResourceEscape.**](mxdcs0pageresourceescape.md)
-   La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve verificarsi tra una chiamata a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), ma possono essere presenti più chiamate di questo tipo tra **le chiamate StartPage** **ed EndPage.**
-   L'utilizzo dello streaming è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP SET S0PAGE RESOURCE come opCode per ogni risorsa nella pagina prima di chiamarla con \_ \_ \_ MXDCOP  \_ SET \_ S0PAGE.

Quando **opCode** è MXDCOP \_ SET \_ XPSPASSTHRU \_ MODE:

-   Il *parametro lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito solo dalla **struttura MXDC ESCAPE HEADER \_ \_ \_ T.**
-   Questa chiamata deve essere eseguita prima della chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

