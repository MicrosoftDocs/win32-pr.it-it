---
description: La funzione DocumentEvent è un gestore eventi per gli eventi associati alla stampa di un documento.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: Funzione DocumentEvent (Winspool.h)
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
ms.openlocfilehash: 0c38a95c4e0dc9820130e467c971c0adb5b9df0ede248506ed56f963c3246b3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971600"
---
# <a name="documentevent-function"></a>Funzione DocumentEvent

La **funzione DocumentEvent** è un gestore eventi per gli eventi associati alla stampa di un documento.

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

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per un oggetto stampante. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*hdc* \[ Pollici\]
</dt> <dd>

Handle del contesto di dispositivo generato da una chiamata di [**CreateDC.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) È zero se *iEsc* è impostato su DOCUMENTEVENT \_ CREATEDCPRE. Per le restrizioni relative alla stampa da un'applicazione a 32 bit in una versione a 64 bit Windows, vedere la sezione Osservazioni.

</dd> <dt>

*iEsc* 
</dt> <dd>

Codice di escape che identifica l'evento da gestire. Questo parametro può essere una delle costanti Integer seguenti.



| Costante                                                                                                                                                                                                                                                                                                                                               | Evento                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | GDI sta per elaborare una chiamata alla [**relativa funzione AbortDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | GDI ha appena elaborato una chiamata alla [**relativa funzione CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o CreateIC.**](/windows/desktop/api/wingdi/nf-wingdi-createica)<br/> Questo codice di escape non deve essere usato a meno che non sia stata precedente una chiamata a **DocumentEvent** con *iEsc* impostato su DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | GDI sta per elaborare una chiamata alla [**relativa funzione CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o CreateIC.**](/windows/desktop/api/wingdi/nf-wingdi-createica)<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | GDI sta per elaborare una chiamata alla [**relativa funzione DeleteDC.**](/windows/desktop/api/wingdi/nf-wingdi-deletedc)<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | GDI ha appena elaborato una chiamata alla [**relativa funzione EndDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | GDI sta per elaborare una chiamata alla [**relativa funzione EndDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | GDI sta per elaborare una chiamata alla [**relativa funzione EndPage.**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | GDI sta per elaborare una chiamata alla relativa [**funzione ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | L'evento DOCUMENTEVENT QUERYFILTER rappresenta un'opportunità per lo spooler di eseguire una query sul driver per ottenere un elenco degli eventi DOCUMENTEVENT XXX a cui \_ \_  risponderà il driver. Questo evento viene generato subito prima di una chiamata a **DocumentEvent** che passa l'evento DOCUMENTEVENT \_ CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | GDI ha appena elaborato una chiamata alla [**relativa funzione ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)<br/> Questo codice di escape non deve essere usato a meno che non sia stata precedente una chiamata a **DocumentEvent** con *iEsc* impostato su DOCUMENTEVENT \_ RESETDCPRE.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | GDI sta per elaborare una chiamata alla [**relativa funzione ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | GDI ha appena elaborato una chiamata alla [**relativa funzione StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | GDI sta per elaborare una chiamata alla [**relativa funzione StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | GDI sta per elaborare una chiamata alla [**relativa funzione StartPage.**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pvIn*.

</dd> <dt>

*pvIn* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer. Il contenuto del buffer dipende dal valore *di iEsc*, come illustrato nella tabella seguente.



| Costante                                                                                                                                                                                                                                                                                                                                               | Contenuto di pvin                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* contiene l'indirizzo di un puntatore alla struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata nel parametro *pvOut* in una chiamata precedente a questa funzione, per cui il parametro *iEsc* è stato impostato su DOCUMENTEVENT \_ CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* punta a una struttura DOCEVENT \_ CREATEDCPRE documentata in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | Non usato.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                                                                                                                                                                     | *pvIn* punta a una struttura \_ DOCEVENT ESCAPE documentata in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Come per DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* contiene l'indirizzo di un puntatore alla struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata nel parametro *pvOut* in una chiamata precedente a questa funzione, per cui il parametro *iEsc* è stato impostato su DOCUMENTEVENT \_ RESETDCPRE.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* contiene l'indirizzo di un puntatore alla [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornita dal chiamante di [**ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn punta* a un long che specifica l'identificatore del processo di stampa restituito da [**StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | *pvIn* contiene l'indirizzo di un puntatore a [**una struttura DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) fornita dal chiamante di [**StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | Non usato.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Valore                       | Significato                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | Dimensione, in byte, del puntatore del buffer a da *pvOut*.                             |
| DOCUMENTEVENT \_ ESCAPE       | Valore utilizzato come parametro *cbOutput* per [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) |
| Per tutti gli altri valori        | *iEsc* non viene usato.                                                                  |



 

</dd> <dt>

*pvOut* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer. Il contenuto del buffer dipende dal valore fornito per *iEsc*, come illustrato nella tabella seguente.



| Costante                                                                                                                                                                                          | Contenuto di pvOut                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornita dal driver, utilizzata da GDI anziché da quella fornita dal [**chiamante CreateDC.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) Se **NULL,** GDI usa la struttura fornita dal chiamante.<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ ESCAPE**</dt> </dl>                | Puntatore a un buffer utilizzato come parametro *lpszOutData* per [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | Puntatore al buffer contenente una struttura DOCEVENT \_ FILTER documentata in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornita dal driver, utilizzata da GDI anziché da quella fornita dal [**chiamante ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) Se **NULL,** GDI usa la struttura fornita dal chiamante.<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito della funzione dipende dall'escape fornito per *iEsc*. Per alcuni codici di escape, il valore restituito non viene usato (vedere di seguito). Se la funzione fornisce un valore restituito, deve essere uno dei seguenti.



| Valore restituito               | Significato                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| ERRORE \_ DOCUMENTEVENT     | Il driver supporta il codice di escape identificato da *iEsc*, ma si è verificato un errore. |
| DOCUMENTEVENT \_ SUCCESS     | Il driver ha gestito correttamente il codice di escape identificato *da iEsc*.             |
| DOCUMENTEVENT \_ NON SUPPORTATO | Il driver non supporta il codice di escape identificato da *iEsc*.                 |



 

L'elenco seguente indica i codici di escape che richiedono un valore restituito e che non lo fanno e spiega il significato dei codici restituiti DOCUMENTEVENT \_ SUCCESS, DOCUMENTEVENT FAILURE e \_ DOCUMENTEVENT \_ UNSUPPORTED.



| Valore restituito                                          | Significato                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ ABORTDOC                               | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | DOCUMENTEVENT FAILURE : GDI non crea il contesto di dispositivo o il contesto delle informazioni e fornisce un valore restituito \_ pari a 0 per [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o CreateIC.**](/windows/desktop/api/wingdi/nf-wingdi-createica) |
| DOCUMENTEVENT \_ DELETEDC                               | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC     | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDPAGE                                | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ ESCAPE                                 | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | Vedere la sezione Osservazioni.                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | Il valore restituito non viene usato e non deve essere letto.                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | DOCUMENTEVENT FAILURE : GDI non reimposta il contesto di dispositivo e fornisce il valore restituito \_ 0 per [**ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | DOCUMENTEVENT \_ FAILURE : GDI chiama [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) per arrestare il documento e quindi fornisce il valore restituito SP \_ ERROR per [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                      |
| DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC | DOCUMENTEVENT FAILURE : GDI non avvia il documento e fornisce il valore restituito \_ SP \_ ERROR per [**StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)                                                       |
| DOCUMENTEVENT \_ STARTPAGE                              | DOCUMENTEVENT FAILURE : GDI non avvia la pagina e fornisce il valore restituito \_ SP \_ ERROR per [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage).                                                         |



 

## <a name="remarks"></a>Commenti

Per un valore *iEsc* di DOCUMENTEVENT QUERYFILTER, lo spooler può interpretare un valore DOCUMENTEVENT SUCCESS restituito da DocumentEvent in due modi, a seconda che il driver modifica alcuni membri della struttura \_ \_ DOCEVENT FILTER (documentata in Windows Driver Development  \_ [Kit).](https://msdn.microsoft.com/windows/hardware/gg487428) Il *parametro pvOut* punta a questa struttura. Quando lo spooler alloca memoria per una struttura di questo tipo, inizializza due membri di questa struttura, **cElementsReturned** e **cElementsNeeded,** a valori noti. Al **termine di DocumentEvent,** lo spooler determina se i valori di questi membri sono stati modificati e usa tali informazioni per interpretare il **valore restituito di DocumentEvent.** La tabella seguente riepiloga questa situazione.



| Valore restituito                          | Stato di cElementsReturned e cElementsNeeded    | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ SUCCESS<br/>     | Il driver non ha apportato modifiche a nessuno dei due membri.<br/> | Lo spooler interpreta questo valore restituito come equivalente a DOCUMENTEVENT \_ UNSUPPORTED. Lo spooler non è in grado di recuperare il filtro eventi dal driver, pertanto persiste nella chiamata **a DocumentEvent** per tutti gli eventi.<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ SUCCESS<br/>     | Il driver ha scritto in uno o entrambi i membri.<br/>    | Lo spooler accetta questo valore restituito senza interpretazione. Se il driver ha scritto solo in uno di **cElementsNeeded** e **cElementsReturned**, lo spooler considera il membro non modificato come valore zero.<br/> Lo spooler filtra tutti gli eventi elencati nel membro **aDocEventCall** di DOCEVENT \_ FILTER (documentato in Windows Driver Development [Kit).](https://msdn.microsoft.com/windows/hardware/gg487428)<br/> |
| DOCUMENTEVENT \_ NON SUPPORTATO<br/> | Non applicabile<br/>                          | Il driver non supporta DOCUMENTEVENT \_ QUERYFILTER.<br/> Lo spooler non è in grado di recuperare il filtro eventi dal driver, pertanto persiste nella chiamata **a DocumentEvent** per tutti gli eventi.<br/>                                                                                                                                                                                                                                            |
| ERRORE \_ DOCUMENTEVENT<br/>     | Non applicabile<br/>                          | Il driver supporta DOCUMENTEVENT \_ QUERYFILTER, ma si è verificato un errore interno.<br/> Lo spooler non è in grado di recuperare il filtro eventi dal driver, pertanto persiste nella chiamata **a DocumentEvent** per tutti gli eventi.<br/>                                                                                                                                                                                                                 |



 

Se il codice di escape fornito nel *parametro iEsc* è DOCUMENTEVENT \_ CREATEDCPRE, si applicano le regole seguenti:

-   Se il processo viene inviato direttamente alla stampante senza spooling, pvIn->pszDevice punta al nome della stampante. Per altre informazioni, vedere la documentazione di DOCEVENT \_ Struttura CREATEDCPRE in [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).
-   Se è in corso lo spooling del processo, pvIn->pszDevice punta al nome della porta della stampante.

> [!Note]  
> Le restrizioni seguenti si applicano quando si esegue un'applicazione a 32 bit in una versione a 64 bit di Windows. L'unica funzione GDI che **DocumentEvent** deve chiamare [**è ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)e devono essere usati solo caratteri di escape privati. **Le chiamate DocumentEvent** ad altre funzioni GDI possono produrre un comportamento non definito.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DocumentEventW** (Unicode) e **DocumentEventA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

