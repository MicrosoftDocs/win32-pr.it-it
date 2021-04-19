---
description: La \_ funzione di escape della stampante MXDC Escape consente alle applicazioni di scrivere documenti in un file o in una stampante in formato XPS (XML Paper Specification) per mezzo di Microsoft XPS Document Converter (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: Funzione MXDC_ESCAPE (MXDC. h)
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
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311820"
---
# <a name="mxdc_escape-function"></a>MXDC \_ escape-funzione

La funzione di escape della stampante **MXDC \_ escape** consente alle applicazioni di scrivere documenti in un file o in una stampante in formato XPS (XML Paper Specification) per mezzo di Microsoft XPS Document Converter (MXDC).

Per eseguire questa operazione, chiamare la funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con i parametri seguenti.

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

*HDC* 
</dt> <dd>

Handle per il contesto di dispositivo stampante.

</dd> <dt>

*cbInput* 
</dt> <dd>

Dimensione, in byte, dei dati a cui punta il parametro *lpszInData* .

</dd> <dt>

*lpszInData* 
</dt> <dd>

Puntatore a un buffer contenente i dati di input, che vengono sempre archiviati in una delle seguenti strutture.

<dl> <dd><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></dd> <dd><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

Ognuna di queste strutture dispone di un membro opcode che specifica le operazioni che MXDC deve eseguire. Per osservazioni dettagliate su questi codici, vedere MxdcEscapeHeader.



| Codice operativo                                                                                                                                                                                                  | Azione                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**MXDCOP \_ ottenere il \_ nome file**</dt> </dl>                                          | Imposta il parametro *lpszOutData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) su, ovvero il percorso completo del file di output come stringa con terminazione zero oppure la dimensione di tale stringa.<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**MXDCOP \_ \_ documento fisso di PRINTTICKET \_ \_**</dt> </dl> | Associa un ticket di stampa a una sequenza di documenti fissa XPS.<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**\_ \_ doc fisso PRINTTICKET \_ MXDCOP**</dt> </dl>              | Associa un ticket di stampa a un documento XPS.<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**\_ \_ pagina fissa PRINTTICKET \_ MXDCOP**</dt> </dl>           | Associa un ticket di stampa a una pagina XPS.<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**MXDCOP \_ set \_ S0PAGE**</dt> </dl>                                                | Invia il markup XPS della pagina corrente all'output.<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**MXDCOP \_ impostare \_ la \_ risorsa S0PAGE**</dt> </dl>                    | Invia all'output una risorsa nella pagina, ad esempio un'immagine o un tipo di carattere.<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**MXDCOP \_ impostare \_ la \_ modalità XPSPASSTHRU**</dt> </dl>                 | Inserisce il MXDC in uno stato di pass-through, consentendo a un'applicazione di scrivere XPS direttamente nel file di output senza alcuna elaborazione da parte di MXDC. In questo modo è possibile scrivere un intero documento o persino una sequenza di documenti.<br/> |



 

</dd> <dt>

*cbOutput* 
</dt> <dd>

Dimensione, in byte, dei dati a cui punta il parametro *lpszOutData* .

</dd> <dt>

*lpszOutData* 
</dt> <dd>

Puntatore a un buffer contenente i dati di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è maggiore di zero. Se la funzione ha esito negativo o non è supportata, il valore restituito è minore o uguale a zero.

## <a name="remarks"></a>Commenti

Questo escape è supportato da MXDC e XPSDrv, ma non da GDI.

Per determinare se il driver della stampante è MXDC, chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con l'escape [**GetTechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Se il driver è MXDC, **ExtEscape** restituirà la stringa con terminazione zero " http://schemas.microsoft.com/xps/2005/06 ". Verificare che il buffer a cui fa riferimento il parametro *lpszOutData* sia sufficientemente grande da contenere questa stringa.

Per determinare se il driver della stampante è il driver Microsoft XPS Document Writer di Windows, verificare che il driver della stampante sia MXDC, quindi determinare se il nome del driver della stampante è "Microsoft XPS Document Writer".

Per ottenere il nome del driver della stampante, utilizzare una delle tecniche seguenti. <dl> Chiamare [**GetPrinterDriver**](getprinterdriver.md) con il valore del parametro *Level* impostato su 1. Il nome del driver della stampante viene restituito nel membro **pname** della struttura di [**informazioni sul driver \_ \_ 1**](driver-info-1.md) .  
oppure  
Chiamare [**GetPrinter**](getprinter.md) con il valore del parametro *Level* impostato su 2. Il nome del driver della stampante viene restituito nel membro **pDriverName** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) .  
</dl>

Nella tabella seguente viene illustrato dove trovare vari oggetti nel file XPS. verranno scritti i vari tipi di oggetti.



| Oggetto       | Posizione nel file di output    |
|--------------|--------------------------------|
| Pagina fissa   | /Documents/1/Pages/Esc%d.fpage |
| Anteprima    | /Documents/1/Metadata          |
| Stampa ticket | /Documents/1/Metadata          |
| Carattere         | /Documents/1/Resources/Fonts   |
| Immagine        | /Documents/1/Resources/Images  |



 

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

[Funzioni di escape della stampante](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

