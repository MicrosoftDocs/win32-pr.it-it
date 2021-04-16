---
description: La funzione DocumentEvent è un gestore eventi per gli eventi associati alla stampa di un documento.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: Funzione DocumentEvent (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentEvent
- DocumentEventA
- DocumentEventW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aa80e5fe17047eceacdc30e2a40a4a629088d89f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529010"
---
# <a name="documentevent-function"></a>DocumentEvent (funzione)

La funzione **DocumentEvent** è un gestore eventi per gli eventi associati alla stampa di un documento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DocumentEvent(
  _In_  HANDLE hPrinter,
  _In_  HDC    hdc,
        INT    iEsc,
        ULONG  cbIn,
  _In_  PVOID  pvIn,
        ULONG  cbOut,
  _Out_ PVOID  pvOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per un oggetto Printer. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*HDC* \[ in\]
</dt> <dd>

Handle di contesto di dispositivo generato da una chiamata a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). Questo valore è zero se *iEsc* è impostato su DOCUMENTEVENT \_ CREATEDCPRE. Per le restrizioni sulla stampa da un'applicazione a 32 bit in una versione di Windows a 64 bit, vedere la sezione Osservazioni.

</dd> <dt>

*iEsc* 
</dt> <dd>

Codice di escape che identifica l'evento da gestire. Questo parametro può essere una delle costanti integer seguenti.



| Costante                                                                                                                                                                                                                                                                                                                                               | Evento                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**\_AbortDoc DOCUMENTEVENT**</dt> </dl>                                                                                                                                                               | GDI sta per elaborare una chiamata alla relativa funzione [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**\_CREATEDCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                   | GDI ha appena elaborato una chiamata alla relativa funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**create**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/> Questo codice di escape non deve essere usato a meno che non esista una precedente chiamata a **DocumentEvent** con *IESC* impostato su DocumentEvent \_ CREATEDCPRE.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**\_CREATEDCPRE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                      | GDI sta per elaborare una chiamata alla relativa funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**create**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**\_DELETEDC DOCUMENTEVENT**</dt> </dl>                                                                                                                                                               | GDI sta per elaborare una chiamata alla relativa funzione [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**\_ENDDOCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                         | GDI ha appena elaborato una chiamata alla relativa funzione [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ EndDoc**</dt> </dl>                 | GDI sta per elaborare una chiamata alla relativa funzione [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**\_ENDPAGE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                  | GDI sta per elaborare una chiamata alla relativa funzione [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**\_escape DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                     | GDI sta per elaborare una chiamata alla relativa funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**\_QUERYFILTER DOCUMENTEVENT**</dt> </dl>                                                                                                                                                      | L' \_ evento DOCUMENTEVENT QUERYFILTER rappresenta un'opportunità per lo spooler di eseguire una query sul driver per un elenco degli \_ eventi DOCUMENTEVENT *xxx* a cui il driver risponderà. Questo evento viene generato immediatamente prima di una chiamata a **DocumentEvent** che passa l' \_ evento DocumentEvent CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**\_RESETDCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                      | GDI ha appena elaborato una chiamata alla relativa funzione [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/> Questo codice di escape non deve essere usato a meno che non esista una precedente chiamata a **DocumentEvent** con *IESC* impostato su DocumentEvent \_ RESETDCPRE.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**\_RESETDCPRE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                         | GDI sta per elaborare una chiamata alla relativa funzione [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**\_STARTDOCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                   | GDI ha appena elaborato una chiamata alla relativa funzione [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ StartDoc**</dt> </dl> | GDI sta per elaborare una chiamata alla relativa funzione [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ Startpage**</dt> </dl>                                                                                                                                                            | GDI sta per elaborare una chiamata alla relativa funzione [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) .<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pvIn*.

</dd> <dt>

*pvIn* \[ in\]
</dt> <dd>

Puntatore a un buffer. Il contenuto del buffer dipende dal valore di *iEsc*, come illustrato nella tabella seguente.



| Costante                                                                                                                                                                                                                                                                                                                                               | Contenuto di PVIN                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**\_AbortDoc DOCUMENTEVENT**</dt> </dl>                                                                                                                                                               | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**\_CREATEDCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                   | *pvIn* contiene l'indirizzo di un puntatore alla struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata nel parametro *pvOut* in una chiamata precedente a questa funzione, per la quale il parametro *iEsc* è stato impostato su DOCUMENTEVENT \_ CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**\_CREATEDCPRE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                      | *pvIn* punta a una \_ struttura CREATEDCPRE di DOCEVENT, documentata in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**\_DELETEDC DOCUMENTEVENT**</dt> </dl>                                                                                                                                                               | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**\_ENDDOCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                         | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ EndDoc**</dt> </dl>                 | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**\_ENDPAGE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                  | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**\_escape DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                     | *pvIn* punta a una \_ struttura di escape DOCEVENT documentata in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**\_QUERYFILTER DOCUMENTEVENT**</dt> </dl>                                                                                                                                                      | Uguale a DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**\_RESETDCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                      | *pvIn* contiene l'indirizzo di un puntatore alla struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata nel parametro *pvOut* in una chiamata precedente a questa funzione, per la quale il parametro *iEsc* è stato impostato su DOCUMENTEVENT \_ RESETDCPRE.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**\_RESETDCPRE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                         | *pvIn* contiene l'indirizzo di un puntatore alla struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornita dal chiamante di [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**\_STARTDOCPOST DOCUMENTEVENT**</dt> </dl>                                                                                                                                                   | *pvIn* punta a un valore Long che specifica l'identificatore del processo di stampa restituito da [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ StartDoc**</dt> </dl> | *pvIn* contiene l'indirizzo di un puntatore a una struttura [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) fornita dal chiamante di [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ Startpage**</dt> </dl>                                                                                                                                                            | Non usato.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Valore                       | Significato                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| \_QUERYFILTER IDOCUMENTEVENT | Dimensione, in byte, del puntatore del buffer a da *pvOut*.                             |
| \_escape DOCUMENTEVENT       | Valore utilizzato come parametro *cbOutput* per [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). |
| Per tutti gli altri valori        | *iEsc* non viene utilizzato.                                                                  |



 

</dd> <dt>

*pvOut* \[ out\]
</dt> <dd>

Puntatore a un buffer. Il contenuto del buffer dipende dal valore specificato per *iEsc*, come illustrato nella tabella seguente.



| Costante                                                                                                                                                                                          | Contenuto di pvOut                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**\_CREATEDCPRE DOCUMENTEVENT**</dt> </dl> | Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornita dal driver, che viene utilizzata da GDI anziché da quella fornita dal chiamante [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . Se **null**, GDI utilizza la struttura fornita dal chiamante.<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**\_escape DOCUMENTEVENT**</dt> </dl>                | Puntatore a un buffer usato come parametro *lpszOutData* per [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**\_QUERYFILTER DOCUMENTEVENT**</dt> </dl> | Puntatore al buffer contenente una struttura di \_ filtro DOCEVENT documentata in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**\_RESETDCPRE DOCUMENTEVENT**</dt> </dl>    | Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornita dal driver, che viene utilizzata da GDI anziché da quella fornita dal chiamante [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) . Se **null**, GDI utilizza la struttura fornita dal chiamante.<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito della funzione dipende dall'escape fornito per *iEsc*. Per alcuni codici di escape, il valore restituito non viene usato (vedere di seguito). Se la funzione fornisce un valore restituito, deve essere uno dei seguenti.



| Valore restituito               | Significato                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_errore DOCUMENTEVENT     | Il driver supporta il codice di escape identificato da *iEsc*, ma si è verificato un errore. |
| DOCUMENTEVENT \_ riuscito     | Il driver ha gestito correttamente il codice di escape identificato da *iEsc*.             |
| DOCUMENTEVENT non \_ supportato | Il driver non supporta il codice di escape identificato da *iEsc*.                 |



 

Nell'elenco seguente sono indicati i codici di escape che richiedono un valore restituito e che non lo sono e spiegano il significato dell' \_ esito positivo del DOCUMENTEVENT, l' \_ errore DOCUMENTEVENT e i codici restituiti DOCUMENTEVENT non \_ supportati.



| Valore restituito                                          | Significato                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_AbortDoc DOCUMENTEVENT                               | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| \_CREATEDCPOST DOCUMENTEVENT                           | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| \_CREATEDCPRE DOCUMENTEVENT                            | \_Errore DOCUMENTEVENT: GDI non crea il contesto di dispositivo o il contesto delle informazioni e fornisce un valore restituito pari a 0 per [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**createal**](/windows/desktop/api/wingdi/nf-wingdi-createica). |
| \_DELETEDC DOCUMENTEVENT                               | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| \_ENDDOCPOST DOCUMENTEVENT                             | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ EndDoc     | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| \_ENDPAGE DOCUMENTEVENT                                | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| \_escape DOCUMENTEVENT                                 | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| \_QUERYFILTER DOCUMENTEVENT                            | Vedere la sezione Osservazioni.                                                                                                                                                                               |
| \_RESETDCPOST DOCUMENTEVENT                            | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| \_RESETDCPRE DOCUMENTEVENT                             | \_Errore DOCUMENTEVENT: GDI non reimposta il contesto di dispositivo e restituisce un valore restituito pari a 0 per [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).                                                           |
| \_STARTDOCPOST DOCUMENTEVENT                           | \_Errore DOCUMENTEVENT-GDI chiama [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) per arrestare il documento e quindi fornisce un valore restituito di errore SP \_ per [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                      |
| DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ StartDoc | \_Errore DOCUMENTEVENT: GDI non avvia il documento e fornisce un valore restituito di \_ errore SP per [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                                                       |
| DOCUMENTEVENT \_ Startpage                              | \_Errore DOCUMENTEVENT: GDI non avvia la pagina e fornisce un valore restituito di \_ errore SP per [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage).                                                         |



 

## <a name="remarks"></a>Commenti

Per un valore *iEsc* di DOCUMENTEVENT \_ QUERYFILTER, lo spooler può interpretare un \_ valore DOCUMENTEVENT Success restituito da **DOCUMENTEVENT** in due modi, a seconda che il driver abbia modificato determinati membri della struttura del \_ filtro DOCEVENT (documentata in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428) ). Il parametro *pvOut* punta a questa struttura. Quando lo spooler alloca memoria per una struttura di questo tipo, inizializza due membri di questa struttura, **cElementsReturned** e **cElementsNeeded**, in valori noti. Dopo la restituzione di **DocumentEvent** , lo spooler determina se i valori di questi membri sono stati modificati e usa tali informazioni per interpretare il valore restituito di **DocumentEvent** . La tabella seguente riepiloga questa situazione.



| Valore restituito                          | Stato di cElementsReturned e cElementsNeeded    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ riuscito<br/>     | Il driver non ha apportato alcuna modifica a entrambi i membri.<br/> | Lo spooler interpreta questo valore restituito come equivalente a DOCUMENTEVENT non \_ supportato. Lo spooler non è in grado di recuperare il filtro eventi dal driver, quindi viene mantenuto nella chiamata a **DocumentEvent** per tutti gli eventi.<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ riuscito<br/>     | Driver scritto su uno o entrambi i membri.<br/>    | Lo spooler accetta questo valore restituito senza interpretazione. Se il driver ha scritto in un solo **cElementsNeeded** e **cElementsReturned**, lo spooler considera il membro non modificato per avere un valore pari a zero.<br/> Lo spooler filtra tutti gli eventi elencati nel membro **aDocEventCall** di DOCEVENT \_ Filter (documentato in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428) ).<br/> |
| DOCUMENTEVENT non \_ supportato<br/> | Non applicabile<br/>                          | Il driver non supporta il \_ QUERYFILTER DOCUMENTEVENT.<br/> Lo spooler non è in grado di recuperare il filtro eventi dal driver, quindi viene mantenuto nella chiamata a **DocumentEvent** per tutti gli eventi.<br/>                                                                                                                                                                                                                                            |
| \_errore DOCUMENTEVENT<br/>     | Non applicabile<br/>                          | Il driver supporta DOCUMENTEVENT \_ QUERYFILTER, ma si è verificato un errore interno.<br/> Lo spooler non è in grado di recuperare il filtro eventi dal driver, quindi viene mantenuto nella chiamata a **DocumentEvent** per tutti gli eventi.<br/>                                                                                                                                                                                                                 |



 

Se il codice di escape fornito nel parametro *iEsc* è DOCUMENTEVENT \_ CREATEDCPRE, si applicano le regole seguenti:

-   Se il processo viene inviato direttamente alla stampante senza spooling, pvIn->pszDevice punta al nome della stampante. Per ulteriori informazioni, vedere la documentazione relativa a DOCEVENT \_ Struttura CREATEDCPRE in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).
-   Se è in corso lo spooling del processo, pvIn->pszDevice punta al nome della porta della stampante.

> [!Note]  
> Quando si esegue un'applicazione a 32 bit in una versione a 64 bit di Windows, si applicano le restrizioni seguenti. L'unica funzione GDI che **DocumentEvent** deve chiamare è [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)ed è necessario usare solo caratteri di escape privati. **DocumentEvent** chiamate ad altre funzioni GDI possono produrre un comportamento indefinito.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DocumentEventW** (Unicode) e **DocumentEventA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

