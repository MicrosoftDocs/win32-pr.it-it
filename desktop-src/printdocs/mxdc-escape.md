---
description: La funzione di escape della stampante MXDC ESCAPE consente alle applicazioni di scrivere documenti in un file o in una stampante \_ in formato XML Paper Specification (XPS) tramite Microsoft XPS Document Converter (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE funzione (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7ace79404808db750a15b2c17b6fedb336dbd1d72b1581888324a4d87bb7cd67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460881"
---
# <a name="mxdc_escape-function"></a>Funzione \_ MXDC ESCAPE

La funzione di escape della stampante **MXDC \_ ESCAPE** consente alle applicazioni di scrivere documenti in un file o in una stampante in formato XML Paper Specification (XPS) tramite Microsoft XPS Document Converter (MXDC).

Per eseguire questa operazione, chiamare la [**funzione ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con i parametri seguenti.

## <a name="syntax"></a>Sintassi


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hdc* 
</dt> <dd>

Handle per il contesto di dispositivo della stampante.

</dd> <dt>

*cbInput* 
</dt> <dd>

Dimensione, in byte, dei dati a cui punta *il parametro lpszInData.*

</dd> <dt>

*lpszInData* 
</dt> <dd>

Puntatore a un buffer contenente i dati di input, che viene sempre archiviato in una delle strutture seguenti.

<dl> <dd><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></dd> <dd><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

Ognuna di queste strutture ha un membro opcode che specifica le operazioni che mxDC deve eseguire. Per informazioni dettagliate su questi codici, vedere MxdcEscapeHeader.



| Codice operativo (opcode)                                                                                                                                                                                                  | Azione                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**MXDCOP \_ GET \_ FILENAME**</dt> </dl>                                          | Imposta il parametro *lpszOutData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) su , il percorso completo del file di output come stringa con terminazione zero oppure le dimensioni di tale stringa.<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ**</dt> </dl> | Associa un ticket di stampa a una sequenza di documenti xps fissa.<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**DOCUMENTAZIONE FISSA DI MXDCOP \_ PRINTTICKET \_ \_**</dt> </dl>              | Associa un ticket di stampa a un documento XPS.<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**PAGINA FISSA DI MXDCOP \_ PRINTTICKET \_ \_**</dt> </dl>           | Associa un print ticket a una pagina XPS.<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**MXDCOP \_ SET \_ S0PAGE**</dt> </dl>                                                | Invia il markup XPS della pagina corrente all'output.<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**MXDCOP \_ SET \_ S0PAGE \_ RESOURCE**</dt> </dl>                    | Invia una risorsa nella pagina, ad esempio un'immagine o un tipo di carattere, all'output.<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**MXDCOP \_ IMPOSTARE LA MODALITÀ \_ XPSPASSTHRU \_**</dt> </dl>                 | Inserisce MXDC in uno stato pass-through, consentendo a un'applicazione di scrivere XPS direttamente nel file di output senza alcuna elaborazione da parte di MXDC. In questo modo è possibile scrivere un intero documento o anche una sequenza di documenti.<br/> |



 

</dd> <dt>

*cbOutput* 
</dt> <dd>

Dimensione, in byte, dei dati a cui punta *il parametro lpszOutData.*

</dd> <dt>

*lpszOutData* 
</dt> <dd>

Puntatore a un buffer contenente i dati di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è maggiore di zero. Se la funzione ha esito negativo o non è supportata, il valore restituito è minore o uguale a zero.

## <a name="remarks"></a>Commenti

Questo escape è supportato da MXDC e XPSDrv, ma non da GDI.

Per determinare se il driver della stampante è MXDC, chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con l'escape [**GETTECHNOLOGY.**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) Se il driver è MXDC, **ExtEscape** restituirà la stringa con terminazione zero, " http://schemas.microsoft.com/xps/2005/06 ". Assicurarsi che il buffer a cui fa riferimento *il parametro lpszOutData* sia sufficientemente grande da contenere questa stringa.

Per determinare se il driver della stampante è il driver Windows in-box Microsoft XPS Document Writer, verificare che il driver della stampante sia MXDC e quindi determinare se il nome del driver della stampante è "Microsoft XPS Document Writer".

Per ottenere il nome del driver della stampante, usare una delle tecniche seguenti. <dl> Chiamare [**GetPrinterDriver con**](getprinterdriver.md) il *valore del* parametro Level impostato su 1. Il nome del driver della stampante viene restituito nel **membro pName** della [**struttura DRIVER INFO \_ \_ 1.**](driver-info-1.md)  
oppure  
Chiamare [**GetPrinter con**](getprinter.md) il *valore del* parametro Level impostato su 2. Il nome del driver della stampante viene restituito nel **membro pDriverName** della [**struttura PRINTER INFO \_ \_ 2.**](printer-info-2.md)  
</dl>

Nella tabella seguente viene illustrato dove trovare vari oggetti nel file XPS in cui verranno scritti vari tipi di oggetti.



| Oggetto       | Percorso nel file di output    |
|--------------|--------------------------------|
| Pagina fissa   | /Documents/1/Pages/Esc%d.fpage |
| Anteprima    | /Documents/1/Metadata          |
| Print Ticket | /Documents/1/Metadata          |
| Carattere         | /Documents/1/Resources/Fonts   |
| Immagine        | /Documents/1/Resources/Images  |



 

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

[Funzioni di escape della stampante](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

