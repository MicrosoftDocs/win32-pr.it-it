---
description: Concede lo stato attendibile della condivisione DDE specificato all'interno del contesto degli utenti corrente.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Funzione NDdeSetTrustedShare (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524954"
---
# <a name="nddesettrustedshare-function"></a>NDdeSetTrustedShare (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Concede lo stato attendibile della condivisione DDE specificato all'interno del contesto dell'utente corrente.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Nome del server di cui è necessario modificare il DSDM.

</dd> <dt>

*lpszShareName* \[ in\]
</dt> <dd>

Nome della condivisione a cui concedere lo stato attendibile. Questo parametro non può essere **null**.

</dd> <dt>

*dwTrustOptions* \[ in\]
</dt> <dd>

Opzioni che interessano lo stato attendibile della condivisione DDE. Questo parametro può avere uno dei valori seguenti.



| Opzione                                                                                                                                                                                                                                                      | Significato                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ Mostra \_ maschera**</dt> <dt>0x0000FFFFL</dt> </dl>             | Maschera utilizzata per ottenere il valore utilizzato per eseguire l'override dello stato di visualizzazione della condivisione DDE, se \_ \_ è impostato NDDE Trust cmd \_ show.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ TRUST \_ cmd \_ Mostra**</dt> <dt>0x10000000L</dt> </dl>          | Eseguire l'override dello stato di visualizzazione specificato nella DSDM della condivisione DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ Condivisione di ATTENDIBILità \_ \_ del**</dt> <dt>0x20000000L</dt> </dl>       | Rimuovere lo stato attendibile della condivisione.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ 0x40000000L \_ \_ init condivisione attendibile**</dt> <dt></dt> </dl>    | Consentire a un client di avviare l'applicazione se è già in esecuzione nel contesto dell'utente.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ 0x80000000L \_ di \_ inizio condivisione attendibilità**</dt> <dt></dt> </dl> | Consente all'applicazione di essere avviata nel contesto dell'utente.<br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Commenti

È innanzitutto necessario creare la condivisione DDE con [**NDDEShareAdd**](nddeshareadd.md).

Se viene chiamato **NDdeSetTrustedShare** con *dwTrustOptions* impostato su zero, la condivisione attendibile perderà lo stato attendibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeSetTrustedShareW** (Unicode) e **NDdeSetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




