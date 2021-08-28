---
title: Modello di schema ADSI
description: Uno schema è simile a un dizionario in quanto contiene la definizione di ogni tipo di oggetto noto a un servizio directory.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI Schema Model ADSI
- ADSI ADSI , about, schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4893151c81eefa0a17420e18d5d87da232641571
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883880"
---
# <a name="adsi-schema-model"></a>Modello di schema ADSI

Uno schema è simile a un dizionario in quanto contiene la definizione di ogni tipo di oggetto noto a un servizio directory. Le applicazioni client ADSI possono esplorare uno schema per individuare le funzionalità di qualsiasi implementazione ADSI specificata. ADSI fornisce anche interfacce di gestione dello schema che possono essere usate per comunicare con lo schema sottostante di un servizio directory.

Alcuni schemi sono estendibili e i provider ADSI o fornitori di terze parti possono scegliere di pubblicare nuove interfacce o proprietà aggiuntive per le interfacce esistenti. I client ADSI usano questi dati per determinare quali funzionalità sono supportate per ogni servizio directory.

Esistono tre tipi di oggetti dello schema: classi, proprietà e sintassi, ognuno dei quali supporta le interfacce di gestione dello schema [**IADsClass,**](/windows/desktop/api/Iads/nn-iads-iadsclass) [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax.**](/windows/desktop/api/Iads/nn-iads-iadssyntax)

> [!Note]  
> La classe è un termine sottoposto a overload. Sono disponibili classi C++, classi Java, classi COM e classi ADSI. In questo documento la parola classe, se non diversamente qualificata, fa riferimento a una categoria o a un tipo di oggetto dello schema.

 

ADSI astrae lo schema di ogni servizio directory e lo inserisce in ogni nodo radice di primo livello **nell'oggetto Namespace.** Per identificare le classi supportate da un servizio directory in un determinato nodo radice, enumerare l'oggetto schema e ottenere un elenco di oggetti classe, oggetti proprietà e oggetti sintassi. Per altre informazioni, vedere [Uso dello schema ADSI.](using-the-adsi-schema.md)

## <a name="adsi-ldap-provider-schema-cache"></a>ADSI LDAP Provider Schema Cache

Il provider LDAP per ADSI tenta di memorizzare nella cache i dati dello schema nel computer locale. Un sottoschema è identificato da un nome distinto archiviato nell'attributo [**subSchemaSubEntry**](/windows/desktop/ADSchema/a-subschemasubentry) che si trova nella radice dell'organizzazione del servizio directory (rootDSE). Oltre a fornire i dati del sottoschema, i server LDAP v3 devono esporre un attributo [**modifyTimeStamp**](/windows/desktop/ADSchema/a-modifytimestamp) usato per determinare l'ultima modifica dello schema.

Quando ADSI viene associato per la prima volta al server LDAP, recupera i dati del sottoschema usando [**l'attributo subSchemaSubEntry.**](/windows/desktop/ADSchema/a-subschemasubentry) Se ADSI riesce a trovare l'oggetto sottoschema, archivia un puntatore ai dati nel Registro di sistema nel computer che si connette al server LDAP. Per informazioni sulla posizione esatta in cui questi valori vengono archiviati nel Registro di sistema, vedere [ADSI e Controllo dell'account utente.](adsi-and-uac.md)

ADSI tenta quindi di elaborare i dati dello schema e legge [**l'attributo modifyTimeStamp.**](/windows/desktop/ADSchema/a-modifytimestamp) Se **l'attributo modifyTimeStamp** esiste e ADSI elabora correttamente lo schema, ADSI scrive il sottoschema su disco e crea i due valori del Registro di sistema seguenti nella chiave . Se i dati del sottoschema esistono, ma non possono essere elaborati, non viene creato nessuno di questi valori del Registro di sistema:

-   Valore **Time** che contiene l'attributo [**modifyTimeStamp.**](/windows/desktop/ADSchema/a-modifytimestamp) Questo valore viene utilizzato per garantire che i dati dello schema siano correnti e impedisca il ricaricamento costante dei dati dello schema.
-   Valore **File** che contiene il percorso in cui ADSI archivia i dati dello schema nel file system. Per impostazione predefinita, ADSI memorizza nella cache il sottoschema nella directory systemroot SchCache con un nome file corrispondente al &lt; &gt; \\ nome del server LDAP.

Se i dati del sottoschema possono essere elaborati, ma non viene esposto alcun attributo [**modifyTimeStamp,**](/windows/desktop/ADSchema/a-modifytimestamp) i dati dello schema vengono memorizzati nella cache in memoria, ma non scritti su disco. Se un server LDAP v3 è stato contattato tramite ADSI nel computer locale e non è presente un sottoschema memorizzato nella cache, è probabilmente per uno dei motivi seguenti:

-   Il server non ha esposto le proprietà corrette.
-   ADSI non è riuscito a elaborare lo schema.
-   ADSI non è riuscito a scrivere il file nel file system.

 

 
