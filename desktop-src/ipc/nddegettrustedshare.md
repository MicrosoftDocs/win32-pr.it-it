---
description: Recupera le opzioni associate a una condivisione DDE presente nell'elenco di utenti del server di condivisioni attendibili.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Funzione NDdeGetTrustedShare (Nddeapi.h)
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
ms.openlocfilehash: 117178118f59c4f8830cab8aee6afc263d169bf58bac5ac81d3e33305b7db9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481931"
---
# <a name="nddegettrustedshare-function"></a>Funzione NDdeGetTrustedShare

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

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

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server in cui risiede DSDM.

</dd> <dt>

*lpszShareName* \[ Pollici\]
</dt> <dd>

Nome della condivisione il cui stato attendibile viene sottoposto a query. Questo parametro non può essere **NULL.**

</dd> <dt>

*lpdwTrustOptions* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le opzioni di attendibilità. Questo parametro non può essere **NULL.** Sono disponibili le opzioni di attendibilità seguenti.



| Valore                                                                                                                                                                                                                                                       | Significato                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ SHOW \_ MASK**</dt> <dt>0x0000FFFFL</dt> </dl>             | Maschera utilizzata per ottenere il valore utilizzato per eseguire l'override dello stato di visualizzazione della condivisione DDE, se l'opzione NDDE \_ TRUST CMD SHOW è \_ \_ impostata.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ TRUST \_ CMD \_ SHOW**</dt> <dt>0x10000000L</dt> </dl>          | Eseguire l'override dello stato di visualizzazione specificato nel DSDM della condivisione DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ DEL**</dt> <dt>0x20000000L</dt> </dl>       | Rimuovere lo stato attendibile della condivisione.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ INIT**</dt> <dt>0x40000000L</dt> </dl>    | Consentire a un client di avviare l'applicazione se è già in esecuzione nel contesto dell'utente.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ TRUST \_ SHARE \_ START**</dt> <dt>0x80000000L</dt> </dl> | Consentire l'avvio dell'applicazione nel contesto dell'utente.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve la prima parte dell'identificatore di modifica della condivisione attendibile. Questo parametro non può essere **NULL.**

</dd> <dt>

*lpdwShareModId1* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve la seconda parte dell'identificatore di modifica della condivisione attendibile. Questo parametro non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString.**](nddegeterrorstring.md)

## <a name="remarks"></a>Commenti

L'identificatore di modifica della condivisione attendibile riflette la versione della condivisione DDE nel DSDM nel momento in cui alla condivisione DDE è stato inizialmente concesso lo stato attendibile. L'identificatore di modifica della condivisione attendibile viene usato principalmente per rimuovere condivisioni attendibili obsolete. Tuttavia, l'utente non deve rimuovere condivisioni attendibili obsolete. L'agente DDE di rete rimuove le condivisioni obsolete per conto dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeGetTrustedShareW** (Unicode) e **NDdeGetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica delle Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 




