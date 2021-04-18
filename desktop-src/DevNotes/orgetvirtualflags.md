---
description: Recupera i flag virtuali nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Funzione ORGetVirtualFlags (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329422"
---
# <a name="orgetvirtualflags-function"></a>ORGetVirtualFlags (funzione)

Recupera i flag virtuali nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Puntatore a una variabile per ricevere i flag di virtualizzazione impostati per la chiave. Dopo la restituzione della funzione, questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**Reg \_ CHIAVE \_ \_ \_ non riuscita**</dt> <dt>4</dt> </dl> | Se questo flag è impostato e un'operazione di apertura non riesce su una chiave abilitata per la virtualizzazione, il registro di sistema non tenta di riaprire la chiave. Se questo flag è chiaro, il registro di sistema tenta di riaprire la chiave con l' \_ accesso massimo consentito.<br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**Reg \_ CHIAVE \_ dont \_ virtualizza**</dt> <dt>2</dt> </dl>     | Se questo flag è impostato e un'operazione di creazione della chiave ha esito negativo perché il chiamante non ha la chiave \_ di creazione della chiave \_ secondaria \_ direttamente nella chiave padre, il registro di sistema non riesce a creare l'operazione. Se questo flag è chiaro, il registro di sistema tenta di creare la chiave nell'archivio virtuale. Il chiamante deve avere la chiave \_ Read right sulla chiave padre.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**Reg \_ \_ \_ Flag di rimaledizione della chiave**</dt> <dt>8</dt> </dl>              | Se questo flag è impostato, i flag di virtualizzazione del registro di sistema vengono propagati dalla chiave padre. Se questo flag è chiaro, i flag di virtualizzazione del registro di sistema non vengono propagati.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

## <a name="remarks"></a>Commenti

La virtualizzazione del registro di sistema è una tecnologia provvisoria per la compatibilità delle applicazioni che consente di reindirizzare le operazioni di scrittura del registro di sistema a posizioni per utente. Questo reindirizzamento è trasparente per le applicazioni che leggono o scrivono nel registro di sistema.

La virtualizzazione del registro di sistema è supportata a partire da Windows Vista. Tuttavia, Microsoft intende rimuoverlo dalle versioni future del sistema operativo Windows, in quanto le altre applicazioni vengono rese compatibili con Windows Vista. Pertanto, le applicazioni non devono dipendere dal comportamento della virtualizzazione del registro di sistema nel sistema.

La virtualizzazione del registro di sistema è abilitata solo per gli elementi seguenti:

-   processi interattivi a 32 bit
-   Chiavi nel **\_ software del \_ computer \\ locale HKEY**
-   Chiavi in cui un amministratore può scrivere

Per ulteriori informazioni, vedere la pagina relativa alla [virtualizzazione del registro](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORSetVirtualFlags**](orsetvirtualflags.md)
</dt> <dt>

[Virtualizzazione del registro di sistema](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
