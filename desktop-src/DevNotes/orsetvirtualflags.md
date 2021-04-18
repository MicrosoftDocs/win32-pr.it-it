---
description: Imposta i flag di virtualizzazione nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: Funzione ORSetVirtualFlags (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: f694d69684a474cfa6d4f6c33c6d8cab7072f605
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324442"
---
# <a name="orsetvirtualflags-function"></a>ORSetVirtualFlags (funzione)

Imposta i flag di virtualizzazione nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro controlla il comportamento del registro di sistema quando un'operazione di creazione o apertura non riesce su una chiave in un hive virtualizzato. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**Reg \_ CHIAVE \_ \_ \_ non riuscita**</dt> <dt>4</dt> </dl> | Se questo flag è impostato e un'operazione di apertura non riesce su una chiave per la quale è abilitata la virtualizzazione, il registro di sistema non tenta di riaprire la chiave. Se questo flag è chiaro, il registro di sistema tenta di riaprire la chiave con l' \_ accesso massimo consentito.<br/>                                                                                    |
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

[**ORGetVirtualFlags**](orgetvirtualflags.md)
</dt> <dt>

[Virtualizzazione del registro di sistema](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
