---
title: Attributi di denominazione utente
description: Gli attributi di denominazione utente identificano gli oggetti utente, ad esempio i nomi di accesso e gli ID utilizzati per motivi di sicurezza.
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- Attributi di denominazione utente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8548178bba8012231a803d476699e8ebb386b6fa9a29015f3721e7b32d94158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185931"
---
# <a name="user-naming-attributes"></a>Attributi di denominazione utente

Gli attributi di denominazione utente identificano gli oggetti utente, ad esempio i nomi di accesso e gli ID utilizzati per motivi di sicurezza. Gli **attributi cn**, **name** e **distinguishedName** sono esempi di attributi di denominazione utente. Un oggetto utente è un oggetto entità di sicurezza, pertanto include anche gli attributi di denominazione utente seguenti:

-   [userPrincipalName:](#userprincipalname) nome di accesso per l'utente
-   [objectGUID:](#objectguid) identificatore univoco di un utente
-   [sAMAccountName:](#samaccountname) nome di accesso che supporta la versione precedente di Windows
-   [objectSid](#objectsid) : ID di sicurezza (SID) dell'utente
-   [sIDHistory:](#sidhistory) i SID precedenti per l'oggetto utente

> [!Note]  
> È possibile visualizzare e gestire questi attributi usando lo snap-in MMC Utenti e computer di Active Directory, disponibile in Strumenti di amministrazione remota del server (Strumenti di amministrazione [remota del server).](https://www.microsoft.com/download/details.aspx?id=45520)

 

## <a name="userprincipalname"></a>userPrincipalName

**L'attributo userPrincipalName** è il nome di accesso per l'utente. L'attributo è costituito da un nome dell'entità utente (UPN), ovvero il nome di accesso più comune per Windows utenti. Gli utenti usano in genere il proprio UPN per accedere a un dominio. Questo attributo è una stringa indicizzata a valore singolo.

Un UPN è un nome di accesso di tipo Internet per un utente basato sullo standard Internet RFC 822. L'UPN è più breve di un nome distinto e più facile da ricordare. Per convenzione, deve eseguire il mapping al nome di posta elettronica dell'utente. Il punto dell'UPN è consolidare gli spazi dei nomi di posta elettronica e di accesso in modo che l'utente deve ricordare un solo nome.

### <a name="upn-format"></a>Formato UPN

Un UPN è costituito da un prefisso UPN (il nome dell'account utente) e un suffisso UPN (nome di dominio DNS). Il prefisso viene unito al suffisso usando il simbolo \"\@\". Ad esempio, "someone@ example.com". Un UPN deve essere univoco tra tutti gli oggetti entità di sicurezza in una foresta di directory. Ciò significa che il prefisso di un UPN può essere riutilizzato, ma non con lo stesso suffisso.

Un suffisso UPN presenta le restrizioni seguenti:

-   Deve essere il nome DNS di un dominio, ma non deve essere il nome del dominio che contiene l'utente.
-   Deve essere il nome di un dominio nella foresta di domini corrente o un nome alternativo elencato nell'attributo **upnSuffixes** del contenitore Partitions all'interno del contenitore Configuration.

### <a name="upn-management"></a>Gestione UPN

Un UPN può essere assegnato, ma non è obbligatorio, quando viene creato un account utente. Quando viene creato, un UPN non è interessato dalle modifiche apportate ad altri attributi dell'oggetto utente, ad esempio l'utente che viene rinominato o spostato. In questo modo l'utente può mantenere lo stesso nome di accesso se una directory viene ristrutturata. Tuttavia, un amministratore può modificare un UPN. Quando si crea un nuovo oggetto utente, è necessario controllare il dominio locale e il catalogo globale per il nome proposto per assicurarsi che non esista già.

Quando un utente usa un UPN per accedere a un dominio, l'UPN viene convalidato eseguendo una ricerca nel dominio locale e quindi nel catalogo globale. Se l'UPN non viene trovato nel catalogo globale, il tentativo di accesso non riesce.

## <a name="objectguid"></a>objectGUID

**L'attributo objectGUID** è l'identificatore univoco di un utente. L'attributo è un identificatore univoco globale (GUID) a 128 bit a valore singolo e viene archiviato come struttura [**ADS \_ OCTET \_ STRING.**](/windows/win32/api/iads/ns-iads-ads_octet_string) Il GUID viene creato dal server Active Directory quando viene creato un oggetto utente.

Poiché il nome distinto di un oggetto cambia se l'oggetto viene rinominato o spostato, il nome distinto non è un identificatore affidabile di un oggetto. In Active Directory Domain Services, l'attributo **objectGUID** di un oggetto non cambia mai, anche se l'oggetto viene rinominato o spostato. È possibile recuperare il formato stringa di **objectGUID** usando il metodo della proprietà **GUID** nei [metodi delle proprietà IADs](/windows/desktop/ADSI/iads-property-methods).

## <a name="samaccountname"></a>sAMAccountName

L'attributo **sAMAccountName** è un nome di accesso usato per supportare client e server della versione precedente di Windows, ad esempio Windows NT 4.0, Windows 95, Windows 98 e LAN Manager. Il nome di accesso deve contenere al massimo 20 caratteri ed essere univoco tra tutti gli oggetti entità di sicurezza all'interno del dominio.

## <a name="objectsid"></a>objectSid

**L'attributo objectSid** è l'ID di sicurezza (SID) dell'utente. Il SID viene usato dal sistema per identificare un utente e le relative appartenenze ai gruppi durante le interazioni con Windows sicurezza. L'attributo è a valore singolo. Il SID è un valore binario univoco usato per identificare l'utente come entità di sicurezza.

Il SID viene impostato dal sistema quando viene creato l'utente. Ogni utente ha un SID univoco rilasciato da un dominio Windows e archiviato **nell'attributo objectSid** dell'oggetto utente nella directory. Ogni volta che un utente accede, il sistema recupera il SID dell'utente dalla directory e lo inserisce nel token di accesso dell'utente. Il SID dell'utente viene usato anche per recuperare i SID per i gruppi di cui l'utente è membro e li inserisce nel token di accesso dell'utente. Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può essere usato nuovamente per identificare un altro utente o gruppo.

## <a name="sidhistory"></a>Sidhistory

**L'attributo sIDHistory** contiene i SID precedenti per l'oggetto utente. Si tratta di un attributo multivalore. Un oggetto utente ha SID precedenti se l'utente è stato spostato in un altro dominio. Ogni volta che un oggetto utente viene spostato in un nuovo dominio, viene creato un nuovo SID a cui viene assegnato l'attributo **objectSid** e il SID precedente viene aggiunto **all'attributo sIDHistory.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi dell'oggetto utente](user-object-attributes.md)
</dt> </dl>

 

 