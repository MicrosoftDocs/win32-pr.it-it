---
description: Recupera le opzioni associate a una condivisione DDE presente nell'elenco utenti del server di condivisioni attendibili.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Funzione NDdeGetTrustedShare (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305713"
---
# <a name="nddegettrustedshare-function"></a>NDdeGetTrustedShare (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Recupera le opzioni associate a una condivisione DDE presente nell'elenco di condivisioni attendibili dell'utente del server.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Nome del server in cui risiede l'DSDM.

</dd> <dt>

*lpszShareName* \[ in\]
</dt> <dd>

Nome della condivisione di cui viene eseguita la query sullo stato attendibile. Questo parametro non può essere **null**.

</dd> <dt>

*lpdwTrustOptions* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le opzioni di attendibilità. Questo parametro non può essere **null**. Sono disponibili le seguenti opzioni di attendibilità.



| Valore                                                                                                                                                                                                                                                       | Significato                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ Mostra \_ maschera**</dt> <dt>0x0000FFFFL</dt> </dl>             | Maschera utilizzata per ottenere il valore utilizzato per eseguire l'override dello stato di visualizzazione della condivisione DDE, se \_ \_ è impostato NDDE Trust cmd \_ show.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ TRUST \_ cmd \_ Mostra**</dt> <dt>0x10000000L</dt> </dl>          | Eseguire l'override dello stato di visualizzazione specificato nella DSDM della condivisione DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ Condivisione di ATTENDIBILità \_ \_ del**</dt> <dt>0x20000000L</dt> </dl>       | Rimuovere lo stato attendibile della condivisione.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ 0x40000000L \_ \_ init condivisione attendibile**</dt> <dt></dt> </dl>    | Consentire a un client di avviare l'applicazione se è già in esecuzione nel contesto dell'utente.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ 0x80000000L \_ di \_ inizio condivisione attendibilità**</dt> <dt></dt> </dl> | Consente all'applicazione di essere avviata nel contesto dell'utente.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve la prima parte dell'identificatore di modifica della condivisione attendibile. Questo parametro non può essere **null**.

</dd> <dt>

*lpdwShareModId1* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve la seconda parte dell'identificatore di modifica della condivisione attendibile. Questo parametro non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Commenti

L'identificatore di modifica della condivisione attendibile riflette la versione della condivisione DDE in DSDM al momento dell'iniziale concessione dello stato attendibile per la condivisione DDE. L'identificatore di modifica della condivisione attendibile viene utilizzato principalmente per rimuovere le condivisioni attendibili obsolete. Tuttavia, l'utente non deve rimuovere le condivisioni attendibili obsolete. L'agente DDE di rete rimuove le condivisioni obsolete per conto dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeGetTrustedShareW** (Unicode) e **NDdeGetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 




