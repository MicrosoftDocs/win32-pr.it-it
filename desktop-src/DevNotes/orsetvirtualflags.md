---
description: Imposta i flag di virtualizzazione sulla chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: Funzione ORSetVirtualFlags (Offreg.h)
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
ms.openlocfilehash: 56ca40b273447c8669c162b8c2dba597f2b2ce98282d40e7b482d04032a5f95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815441"
---
# <a name="orsetvirtualflags-function"></a>Funzione ORSetVirtualFlags

Imposta i flag di virtualizzazione sulla chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Handle* \[ Pollici\]
</dt> <dd>

Handle per una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro controlla il comportamento del Registro di sistema quando un'operazione Create o Open non riesce su una chiave in un hive virtualizzato. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**REG \_ KEY \_ DONT \_ SILENT \_ FAIL**</dt> <dt>4</dt> </dl> | Se questo flag è impostato e un'operazione Open non riesce su una chiave per cui è abilitata la virtualizzazione, il Registro di sistema non tenta di riaprire la chiave. Se questo flag è deselezionato, il Registro di sistema tenta di riaprire la chiave con l'accesso MAXIMUM \_ ALLOWED.<br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**REG \_ KEY \_ DONT \_ VIRTUALIZE**</dt> <dt>2</dt> </dl>     | Se questo flag è impostato e un'operazione Di creazione chiave ha esito negativo perché il chiamante non dispone del diritto KEY CREATE SUB KEY sulla chiave padre, il Registro di sistema ha esito negativo per \_ \_ l'operazione \_ Create. Se questo flag è deselezionato, il Registro di sistema tenta di creare la chiave nell'archivio virtuale. Il chiamante deve disporre del diritto KEY \_ READ sulla chiave padre.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**REG \_ FLAG \_ DI RICORSIONE \_ CHIAVE**</dt> <dt>8</dt> </dl>              | Se questo flag è impostato, i flag di virtualizzazione del Registro di sistema vengono propagati dalla chiave padre. Se questo flag è deselezionato, i flag di virtualizzazione del Registro di sistema non vengono propagati.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

## <a name="remarks"></a>Commenti

La virtualizzazione del Registro di sistema è una tecnologia provvisoria di compatibilità delle applicazioni che consente di reindirizzare le operazioni di scrittura del Registro di sistema con impatto globale a percorsi per utente. Questo reindirizzamento è trasparente per le applicazioni che leggono o scrivono nel Registro di sistema.

La virtualizzazione del Registro di sistema è supportata a partire Windows Vista. Tuttavia, Microsoft intende rimuoverlo dalle versioni future del sistema operativo Windows in quanto vengono rese compatibili più applicazioni con Windows Vista. Pertanto, le applicazioni non devono dipendere dal comportamento della virtualizzazione del Registro di sistema nel sistema.

La virtualizzazione del Registro di sistema è abilitata solo per gli elementi seguenti:

-   Processi interattivi a 32 bit
-   Chiavi nel **software HKEY \_ LOCAL \_ MACHINE \\**
-   Chiavi in cui un amministratore può scrivere

Per altre informazioni, vedere [Registry Virtualization](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORGetVirtualFlags**](orgetvirtualflags.md)
</dt> <dt>

[Virtualizzazione del Registro di sistema](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
