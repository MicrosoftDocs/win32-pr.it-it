---
description: Crea un oggetto contesto che descrive il dispositivo tablet specificato.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: Metodo ITablet::CreateContext
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
ms.openlocfilehash: 8b67e4c15d40f2da7a616295f10a7762b242fb40d9c0b5f42c00eb51d190cc03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450576"
---
# <a name="itabletcreatecontext-method"></a>Metodo ITablet::CreateContext

Crea un oggetto contesto che descrive il dispositivo tablet specificato.

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

*hWnd* \[ Pollici\]
</dt> <dd>

Finestra a cui verrà collegato il contesto del tablet.

</dd> <dt>

*prcInput* \[ Pollici\]
</dt> <dd>

\[in, univoco\]

Rettangolo di input penna.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Flag che impostano le opzioni del contesto del tablet.

</dd> <dt>

*pTCS* \[ Pollici\]
</dt> <dd>

\[in, univoco\]

Informazioni dettagliate sul contesto del tablet da creare.

</dd> <dt>

*cet* \[ Pollici\]
</dt> <dd>

Valore che abilita o disabilita i messaggi di contesto inviati alla finestra.

</dd> <dt>

*ppCtx* \[ Cambio\]
</dt> <dd>

Puntatore al contesto del tablet appena creato.

</dd> <dt>

*pTcid* \[ in, out\]
</dt> <dd>

Valore che identifica in modo univoco il tablet.

</dd> <dt>

*ppPD* \[ in, out\]
</dt> <dd>

Puntatore a informazioni sui dati contenuti in ogni pacchetto.

</dd> <dt>

*pSink* \[ Pollici\]
</dt> <dd>

Oggetto [**ITabletEventSink**](itableteventsink.md) a cui verranno inviati i messaggi di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

In genere, un'applicazione ottiene i valori predefiniti dal metodo [**ITablet::GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica i valori in base alle proprie esigenze e quindi passa la struttura delle impostazioni modificata al metodo **ITablet::CreateContext**.

> [!Note]  
> È necessario implementare [**l'interfaccia ITabletEventSink**](itableteventsink.md) quando si chiama il metodo **ITablet::CreateContext**.

 

Il *parametro dwOptions* è un set di flag di bit che descrivono le opzioni di contesto. Nella tabella seguente vengono descritti questi flag.



| Nome flag                                | Valore                                                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MARGINE TCXO \_<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Specifica che il contesto di input nel tablet avrà un margine. Il margine è un'area esterna all'area di input specificata in cui verrà eseguito il mapping degli eventi al bordo dell'area di input. Questa funzionalità semplifica l'immissione di punti sul bordo del contesto.<br/> |
| TCXO \_ PREHOOK<br/>                 | 0x00000002<br/>                                                                                                                                                                         | Il prehook ottiene i pacchetti prima dei contesti regolari e dei posthook. Ottengono pacchetti nell'ordine di creazione.<br/>                                                                                                                                                  |
| STATO CURSORE TCXO \_ \_<br/>           | 0x00000004<br/>                                                                                                                                                                         | Il TC restituirà pacchetti anche se il cursore è verso l'alto. Per impostazione predefinita, un TC restituirà pacchetti solo quando il cursore è in basso.<br/>                                                                                                                                       |
| TCXO \_ NO \_ CURSOR \_ DOWN<br/>        | 0x00000008<br/>                                                                                                                                                                         | Il TC non restituirà pacchetti quando il cursore è in basso.<br/>                                                                                                                                                                                                       |
| TCXO \_ NON \_ INTEGRATO<br/>         | 0x00000010<br/>                                                                                                                                                                         | Il contesto non sarà integrato.<br/>                                                                                                                                                                                                                           |
| TCXO \_ POSTHOOK<br/>                | 0x00000020<br/>                                                                                                                                                                         | I posthook ottengono pacchetti dopo i normali contesti tablet, ma prima del contesto di sistema. Ottengono i pacchetti nell'ordine inverso della creazione.<br/>                                                                                                                   |
| TCXO \_ DONT \_ SHOW \_ CURSOR<br/>      | 0x00000080<br/>                                                                                                                                                                         | TC non imposta la posizione del cursore.<br/>                                                                                                                                                                                                                      |
| TCXO \_ DONT \_ VALIDATE \_ TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | TC non convaliderà i GUID passati nelle impostazioni del contesto del tablet rispetto alle proprietà supportate del dispositivo.<br/>                                                                                                                                      |
| TCXO \_ ALLOW \_ FLICKS<br/>           | 0x00000400<br/>                                                                                                                                                                         | Il TC consentirà di eseguire il rilevamento dello scorrimento (per impostazione predefinita è consentito solo nei contesti di sistema) e il client otterrà edizione Standard \_ eventi FLICK.<br/>                                                                                                               |
| TCXO \_ ALLOW \_ FEEDBACK \_ TAPS<br/>   | 0x00000800<br/>                                                                                                                                                                         | Il TC consentirà di visualizzare il feedback della penna. Per impostazione predefinita, questa opzione è consentita solo nei contesti di sistema.<br/>                                                                                                                                                              |
| TCXO \_ ALLOW \_ FEEDBACK \_ AFFRESE<br/> | 0x00001000<br/>                                                                                                                                                                         | Il TC consentirà di visualizzare il feedback della penna. Per impostazione predefinita, questa opzione è consentita solo nei contesti di sistema.<br/>                                                                                                                                                              |
| TCXO \_ ALL<br/>                     | TCXO \_ MARGIN \| TCXO \_ PREHOOK \| TCXO \_ CURSOR \_ STATE \| TCXO \_ NO \_ CURSOR \_ DOWN \| TCXO \_ NON \_ INTEGRATED \| TCXO \_ POSTHOOK \| TCXO \_ DONT \_ SHOW \_ CURSOR \| TCXO \_ DONT \_ VALIDATE \_ TCS<br/> | Tutte le opzioni del contesto del tablet definite.<br/>                                                                                                                                                                                                                           |
| TCXO \_ HOOK<br/>                    | TCXO \_ PREHOOK \| TCXO \_ POSTHOOK<br/>                                                                                                                                                    | Combina funzionalità pre-hook e post-hook.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> <dt>

[**Enumerazione CONTEXT \_ ENABLE \_ TYPE**](context-enable-type.md)
</dt> <dt>

[**Struttura TABLET \_ CONTEXT \_ SETTINGS**](tablet-context-settings.md)
</dt> <dt>

[**Struttura PACKET \_ DESCRIPTION**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**Interfaccia ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




