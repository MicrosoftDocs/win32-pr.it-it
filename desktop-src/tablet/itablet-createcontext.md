---
description: Crea un oggetto di contesto che descrive il dispositivo Tablet specificato.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'Metodo ITablet:: CreateContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884929"
---
# <a name="itabletcreatecontext-method"></a>Metodo ITablet:: CreateContext

Crea un oggetto di contesto che descrive il dispositivo Tablet specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

La finestra alla quale verrà collegato il contesto della tavoletta.

</dd> <dt>

*prcInput* \[ in\]
</dt> <dd>

\[in, univoco\]

Rettangolo di input dell'input penna.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Flag che impostano le opzioni del contesto del tablet.

</dd> <dt>

*pTCS* \[ in\]
</dt> <dd>

\[in, univoco\]

Informazioni dettagliate sul contesto del tablet da creare.

</dd> <dt>

*CET* \[ in\]
</dt> <dd>

Valore che Abilita o Disabilita i messaggi di contesto inviati alla finestra.

</dd> <dt>

*ppCtx* \[ out\]
</dt> <dd>

Puntatore al nuovo contesto di creazione della tavoletta.

</dd> <dt>

*pTcid* \[ in uscita\]
</dt> <dd>

Valore che identifica in modo univoco il tablet.

</dd> <dt>

*ppPD* \[ in uscita\]
</dt> <dd>

Puntatore alle informazioni sui dati contenuti in ogni pacchetto.

</dd> <dt>

*pSink* \[ in\]
</dt> <dd>

Oggetto [**ITabletEventSink**](itableteventsink.md) in cui verranno inviati i messaggi di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

In genere, un'applicazione ottiene i valori predefiniti dal [**Metodo ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica i valori in base alle proprie esigenze e quindi passa la struttura delle impostazioni modificate al **Metodo ITablet:: CreateContext**.

> [!Note]  
> È necessario implementare l' [**interfaccia ITabletEventSink**](itableteventsink.md) quando si chiama il **Metodo ITablet:: CreateContext**.

 

Il parametro *dwOptions* è un set di flag di bit che descrivono le opzioni di contesto. Nella tabella seguente vengono descritti questi flag.



| Nome del flag                                | Valore                                                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_margine TCXO<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Specifica che il contesto di input nel Tablet avrà un margine. Il margine è un'area al di fuori dell'area di input specificata in cui verrà eseguito il mapping degli eventi al bordo dell'area di input. Questa funzionalità rende più semplice l'input dei punti al bordo del contesto.<br/> |
| prehook TCXO \_<br/>                 | 0x00000002<br/>                                                                                                                                                                         | Il prehook ottiene i pacchetti prima di contesti e posthook regolari. Ottengono i pacchetti nell'ordine di creazione.<br/>                                                                                                                                                  |
| \_stato cursore \_ TCXO<br/>           | 0x00000004<br/>                                                                                                                                                                         | Il TC restituirà i pacchetti anche se il cursore è attivo. Per impostazione predefinita, un TC restituirà pacchetti solo quando il cursore è inattivo.<br/>                                                                                                                                       |
| TCXO \_ senza \_ cursore in \_ basso<br/>        | 0x00000008<br/>                                                                                                                                                                         | Il TC non restituirà pacchetti quando il cursore non è attivo.<br/>                                                                                                                                                                                                       |
| TCXO \_ non \_ integrato<br/>         | 0x00000010<br/>                                                                                                                                                                         | Il contesto non sarà integrato.<br/>                                                                                                                                                                                                                           |
| TCXO \_ POSThook<br/>                | 0x00000020<br/>                                                                                                                                                                         | I posthook ottengono i pacchetti dopo i normali contesti di tablet ma prima del contesto di sistema. Ottengono i pacchetti nell'ordine inverso rispetto alla loro creazione.<br/>                                                                                                                   |
| TCXO \_ non \_ Mostra \_ cursore<br/>      | 0x00000080<br/>                                                                                                                                                                         | Il TC non imposterà la posizione del cursore.<br/>                                                                                                                                                                                                                      |
| TCXO \_ dont \_ Validate \_ TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | Il TC non convaliderà i GUID passati nelle impostazioni di contesto del tablet per le proprietà supportate del dispositivo.<br/>                                                                                                                                      |
| TCXO \_ consentire i \_ gesti rapidi<br/>           | 0x00000400<br/>                                                                                                                                                                         | Il TC consentirà il rilevamento dei gesti rapidi (per impostazione predefinita è consentito solo nei contesti di sistema) e il client otterrà \_ gli eventi Flick.<br/>                                                                                                               |
| TCXO \_ consentire \_ i \_ rubinetti dei commenti<br/>   | 0x00000800<br/>                                                                                                                                                                         | Il TC consentirà di visualizzare il feedback della penna. Per impostazione predefinita, questa opzione è consentita solo nei contesti di sistema.<br/>                                                                                                                                                              |
| TCXO \_ Consenti \_ feedback \_ Barrel<br/> | 0x00001000<br/>                                                                                                                                                                         | Il TC consentirà di visualizzare il feedback della penna. Per impostazione predefinita, questa opzione è consentita solo nei contesti di sistema.<br/>                                                                                                                                                              |
| TCXO \_ tutto<br/>                     | TCXO \_ margin \| TCXO \_ prehook \| TCXO \_ Cursor \_ state \| TCXO \_ No \_ Cursor \_ down \| TCXO \_ non \_ Integrated \| TCXO \_ posthook \| TCXO \_ dont \_ Show \_ Cursor \| TCXO \_ dont \_ Validate \_ TCS<br/> | Tutte le opzioni di contesto del Tablet definite.<br/>                                                                                                                                                                                                                           |
| \_hook TCXO<br/>                    | TCXO \_ prehook \| TCXO \_<br/>                                                                                                                                                    | Combina la funzionalità di pre-Hook e post-hook.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> <dt>

[**\_Enumerazione del tipo abilitata per il contesto \_**](context-enable-type.md)
</dt> <dt>

[**\_ \_ Struttura delle impostazioni di contesto del Tablet**](tablet-context-settings.md)
</dt> <dt>

[**\_Struttura di descrizione pacchetti**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**Interfaccia ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




