---
description: Usato per rappresentare le voci del Registro di sistema che controllano la memorizzazione nella cache delle chiavi private da parte di CSP basati su software Microsoft.
ms.assetid: 67909072-72fe-4777-ae52-a7b9047c9dd5
title: Costanti Caching chiave privata (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d4caf6a3973a5113e03cbe24882241609ff83b8be65a20492f8f967abb734f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978562"
---
# <a name="private-key-caching-constants"></a>Costanti Caching private key

Le costanti seguenti vengono usate per rappresentare le voci del Registro di sistema che controllano la [*memorizzazione*](../secgloss/p-gly.md) nella cache delle chiavi private da parte di CSP basati su software Microsoft.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span id="szKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><span id="szkey_cryptoapi_private_key_options"></span><span id="SZKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><dl> <dt>**szKEY \_ CRYPTOAPI \_ PRIVATE \_ KEY \_ OPTIONS**</dt> <dt>"Criteri software Crittografia \\ \\ \\ \\ \\ \\ Microsoft"</dt> </dl> | Percorso, nella radice **HKEY \_ LOCAL \_ MACHINE,** delle voci del Registro di sistema di memorizzazione nella cache della chiave privata.<br/> |



Le costanti seguenti vengono usate per identificare i valori del Registro di sistema che controllano la memorizzazione nella cache delle chiavi private a livello globale per un processo specifico da parte di CSP basati su software Microsoft.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="szPRIV_KEY_CACHE_MAX_ITEMS"></span><span id="szpriv_key_cache_max_items"></span><span id="SZPRIV_KEY_CACHE_MAX_ITEMS"></span><dl> <dt>**szPRIV \_ KEY \_ CACHE \_ MAX \_ ITEMS**</dt> <dt>"PrivKeyCacheMaxItems"</dt> </dl>                                                                  | Valore **\_ DWORD REG** nella chiave del Registro di sistema **szKEY \_ CRYPTOAPI \_ PRIVATE KEY \_ \_ OPTIONS** che specifica il numero massimo di chiavi private che possono essere memorizzate nella cache contemporaneamente per un singolo processo. Questo controllo viene eseguito ogni volta che viene letta una chiave privata archiviata. Se viene superato il numero massimo, la chiave usata meno di recente viene rimossa dalla cache.<br/> Se questo valore è zero, nessuna chiave viene memorizzata nella cache. Se questo valore non è presente, come valore predefinito viene usato il valore **predefinito cPRIV \_ KEY CACHE MAX ITEMS \_ \_ \_ \_ DEFAULT.**<br/> Se a una chiave privata eliminata dalla cache viene fatto riferimento in un contesto aperto, la chiave viene letta dall'archiviazione al successivo tentativo di usare la chiave.<br/> **Windows Server 2003 e Windows XP con SP1 e versioni precedenti:** Questo valore del Registro di sistema non è supportato.<br/>                                  |
| <span id="cPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><span id="cpriv_key_cache_max_items_default"></span><span id="CPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><dl> <dt>**cPRIV \_ KEY \_ CACHE MAX ITEMS \_ \_ \_ DEFAULT**</dt> <dt>20</dt> </dl>                                                         | Valore predefinito della voce del Registro di sistema **szPRIV \_ KEY CACHE MAX \_ \_ \_ ITEMS** se non viene specificato alcun valore.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="szPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><span id="szpriv_key_cache_purge_interval_seconds"></span><span id="SZPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><dl> <dt>**szPRIV \_ KEY \_ CACHE \_ PURGE INTERVAL \_ \_ SECONDS**</dt> <dt>"PrivKeyCachePurgeIntervalSeconds"</dt> </dl> | Valore **\_ DWORD REG** nella chiave del Registro di sistema **szKEY \_ CRYPTOAPI \_ PRIVATE KEY \_ \_ OPTIONS** che specifica la validità massima, in secondi, di qualsiasi chiave privata memorizzata nella cache. Questo controllo viene eseguito ogni volta che viene usata o letta una chiave privata archiviata. Se questa quantità di tempo è trascorsa dall'ultima cancellazione, tutte le chiavi memorizzate nella cache a cui non è stato fatto riferimento dopo l'ultima cancellazione verranno rimosse dalla cache.<br/> Se questo valore non è presente, come valore predefinito viene usato il valore **predefinito cPRIV \_ KEY CACHE \_ \_ PURGE INTERVAL \_ \_ SECONDS \_** DEFAULT.<br/> Se a una chiave privata cancellata dalla cache viene fatto riferimento in un contesto aperto, la chiave verrà letta dall'archiviazione al successivo tentativo di usare la chiave.<br/> **Windows Server 2003 e Windows XP con SP1 e versioni precedenti:** Questo valore del Registro di sistema non è supportato.<br/> |
| <span id="cPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><span id="cpriv_key_cache_purge_interval_seconds_default"></span><span id="CPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><dl> <dt>**cPRIV \_ INTERVALLO \_ DI \_ RIPULITURA \_ CACHE CHIAVI SECONDI \_ \_ PREDEFINITO**</dt> <dt>86400</dt> </dl> | Valore predefinito della voce del Registro di sistema **szPRIV \_ KEY \_ CACHE \_ PURGE INTERVAL \_ \_ SECONDS** se non viene specificato alcun valore. Questo valore equivale a un giorno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



Le costanti seguenti vengono usate per identificare i valori del Registro di sistema che controllano la memorizzazione nella cache delle chiavi private per una singola istanza del [*provider*](../secgloss/c-gly.md) del servizio di crittografia basato su software Microsoft.



| Costante/valore                                                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>"AllowCachePW"</dt> </dl>                                                                                                                                                         | Valore **\_ DWORD REG** nella chiave del Registro di sistema **HKEY LOCAL MACHINE SOFTWARE \_ Policies Microsoft \_ \\ \\ \\ \\ Cryptography \\ Protect** che specifica se la memorizzazione nella cache delle password è abilitata per le chiavi protette da password nei CSP basati su software Microsoft. Se questo valore è 0, la memorizzazione nella cache delle password viene disabeled e all'utente viene richiesta la password ogni volta che viene usata una chiave protetta da password. Qualsiasi altro valore, o l'assenza di questo valore, indica che la password verrà memorizzata nella cache. In questo scenario, all'utente viene richiesto solo una volta per ogni processo per ogni chiave. <br/> |
| <span id="szKEY_CACHE_ENABLED"></span><span id="szkey_cache_enabled"></span><span id="SZKEY_CACHE_ENABLED"></span><dl> <dt>**szKEY \_ CACHE \_ ENABLED**</dt> <dt>"CachePrivateKeys"</dt> </dl>          | Valore **\_ DWORD REG** nella chiave del Registro di sistema **szKEY \_ CRYPTOAPI \_ PRIVATE KEY \_ \_ OPTIONS** che specifica se la memorizzazione nella cache delle chiavi private è abilitata. Se questo valore è 1, la memorizzazione nella cache della chiave privata è abilitata. Qualsiasi altro valore, o l'assenza di questo valore, indica che la memorizzazione nella cache della chiave privata è disabilitata.<br/> **Windows Vista con SP1, Windows Vista e Windows XP:** Questo valore del Registro di sistema non è supportato.<br/>                                                                                                                                                        |
| <span id="szKEY_CACHE_SECONDS"></span><span id="szkey_cache_seconds"></span><span id="SZKEY_CACHE_SECONDS"></span><dl> <dt>**szKEY \_ CACHE \_ SECONDS**</dt> <dt>"PrivateKeyLifetimeSeconds"</dt> </dl> | Valore **\_ DWORD REG** nella chiave del Registro di sistema **szKEY \_ CRYPTOAPI \_ PRIVATE KEY \_ \_ OPTIONS** che specifica la validità massima, in secondi, di qualsiasi chiave privata memorizzata nella cache.<br/> **Windows XP:** Questo valore del Registro di sistema non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

Le differenze tra i valori **szKEY \_ CACHE \_ SECONDS e** **szPRIV \_ KEY CACHE \_ \_ PURGE INTERVAL \_ \_ SECONDS** sono le seguenti:

 **szKEY \_ CACHE \_ SECONDS**  

-   Questo valore si applica solo a un CSP specifico. Dopo il rilascio del provider di servizi di configurazione, viene rilasciata anche la cache del provider di servizi di configurazione.  
-   Questo valore viene applicato solo quando si tenta di usare una chiave privata specifica con un handle di contesto specifico.  

**szPRIV \_ KEY \_ CACHE \_ PURGE INTERVAL \_ \_ SECONDS**  

-   Questo valore si applica a tutti i CSP in un processo. Anche se il provider di servizi di configurazione viene rilasciato, questa cache non viene rilasciata.  
-   Questo valore si applica ogni volta che una chiave privata archiviata viene usata o letta dall'archiviazione in un singolo processo.  



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
