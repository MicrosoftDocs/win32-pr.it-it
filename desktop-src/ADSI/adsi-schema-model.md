---
title: Modello di schema ADSI
description: Uno schema è simile a un dizionario in quanto include la definizione di ogni tipo di oggetto noto a un servizio directory.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI schema Model ADSI
- ADSI ADSI, informazioni su, schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23eec9264ae2692952106802cc06cbad937a42a9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963451"
---
# <a name="adsi-schema-model"></a>Modello di schema ADSI

Uno schema è simile a un dizionario in quanto include la definizione di ogni tipo di oggetto noto a un servizio directory. Le applicazioni client ADSI possono esplorare uno schema per individuare le funzionalità di qualsiasi implementazione ADSI specificata. ADSI fornisce inoltre interfacce di gestione dello schema che possono essere usate per comunicare con lo schema sottostante di un servizio directory.

Alcuni schemi sono provider estendibili e ADSI oppure i fornitori di terze parti possono scegliere di pubblicare nuove interfacce o proprietà aggiuntive per le interfacce esistenti. I client ADSI utilizzano questi dati per determinare quali funzionalità sono supportate per ogni servizio directory.

Esistono tre tipi di oggetti dello schema: classi, proprietà e sintassi, ciascuno dei quali supporta rispettivamente le interfacce di gestione dello schema [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

> [!Note]  
> La classe è un termine di overload. Sono disponibili classi C++, classi Java, classi COM e classi ADSI. In questo documento, la parola classe, a meno che non sia diversamente qualificato, fa riferimento a una categoria o a un tipo di oggetto dello schema.

 

ADSI estrae lo schema di ogni servizio directory e lo inserisce in ogni nodo radice di primo livello nell'oggetto **spazio dei nomi** . Per identificare le classi supportate da un servizio directory in un nodo radice specifico, è necessario enumerare l'oggetto dello schema e ottenere un elenco di oggetti classe, oggetti proprietà e oggetti sintassi. Per ulteriori informazioni, vedere [utilizzo dello schema ADSI](using-the-adsi-schema.md).

## <a name="adsi-ldap-provider-schema-cache"></a>Cache dello schema del provider LDAP ADSI

Il provider LDAP per ADSI tenta di memorizzare nella cache i dati dello schema nel computer locale. Un sottoschema viene identificato da un nome distinto archiviato nell'attributo [**subschemaSubentry**](/windows/desktop/ADSchema/a-subschemasubentry) che si trova nella radice di Directory Service Enterprise (RootDSE). Oltre a fornire i dati di sottoschema, i server LDAP v3 devono esporre un attributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) usato per determinare l'ultima modifica dello schema.

Quando ADSI viene prima associato al server LDAP, recupera i dati di sottoschema usando l'attributo [**subschemaSubentry**](/windows/desktop/ADSchema/a-subschemasubentry) . Se ADSI riesce a trovare l'oggetto sottoschema, archivia un puntatore ai dati nel registro di sistema del computer che si connette al server LDAP. Per informazioni sulla posizione esatta in cui questi valori vengono archiviati nel registro di sistema, vedere [ADSI e controllo dell'account utente](adsi-and-uac.md).

ADSI tenta quindi di elaborare i dati dello schema e di leggere l'attributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Se l'attributo **modifyTimeStamp** esiste e ADSI elabora lo schema, ADSI scrive il sottoschema sul disco e crea i due valori del registro di sistema seguenti sotto la chiave. Se i dati di sottoschema esistono, ma non possono essere elaborati, nessuno dei valori del registro di sistema viene creato:

-   Valore di **ora** , che contiene l'attributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) . Questo valore viene utilizzato per garantire che i dati dello schema siano aggiornati e impedisce il ricaricamento costante dei dati dello schema.
-   Valore del **file** che contiene il percorso in cui ADSI archivia i dati dello schema nel file System. Per impostazione predefinita, ADSI memorizza nella cache il sottoschema nella <systemroot> \\ directory SchCache con un nome file corrispondente al nome del server LDAP.

Se è possibile elaborare i dati di sottoschema, ma non viene esposto alcun attributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) , i dati dello schema vengono memorizzati nella cache in memoria, ma non vengono scritti su disco. Se un server LDAP v3 è stato contattato tramite ADSI nel computer locale e non è presente un sottoschema memorizzato nella cache, è molto probabile per uno dei motivi seguenti:

-   Il server non ha esposto le proprietà corrette.
-   ADSI non è stato in grado di elaborare lo schema.
-   ADSI non è stato in grado di scrivere il file nel file system.

 

 