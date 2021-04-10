---
title: Attributi di denominazione utente
description: Gli attributi di denominazione utente identificano gli oggetti utente, ad esempio i nomi di accesso e gli ID usati per motivi di sicurezza.
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- Attributi di denominazione utente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a504070cf2e78cf5647072ff740d137b4a6e6056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956311"
---
# <a name="user-naming-attributes"></a>Attributi di denominazione utente

Gli attributi di denominazione utente identificano gli oggetti utente, ad esempio i nomi di accesso e gli ID usati per motivi di sicurezza. Gli attributi **CN**, **Name** e **Distinguishname** sono esempi di attributi di denominazione utente. Un oggetto utente è un oggetto entità di sicurezza, quindi include anche gli attributi di denominazione utente seguenti:

-   [userPrincipalName](#userprincipalname) : nome di accesso per l'utente
-   [objectGUID](#objectguid) : identificatore univoco di un utente
-   [sAMAccountName](#samaccountname) : un nome di accesso che supporta la versione precedente di Windows
-   [objectSID](#objectsid) : ID di sicurezza (SID) dell'utente
-   [sIDHistory](#sidhistory) -i SID precedenti per l'oggetto utente

> [!Note]  
> È possibile visualizzare e gestire questi attributi usando lo snap-in MMC utente e computer Active Directory, disponibile nella [strumenti di amministrazione remota del server (strumenti di amministrazione remota](https://www.microsoft.com/download/details.aspx?id=45520)del server).

 

## <a name="userprincipalname"></a>userPrincipalName

L'attributo **userPrincipalName** è il nome di accesso per l'utente. L'attributo è costituito da un nome dell'entità utente (UPN), che rappresenta il nome di accesso più comune per gli utenti di Windows. Gli utenti usano in genere il proprio UPN per accedere a un dominio. Questo attributo è una stringa indicizzata a valore singolo.

Un UPN è un nome di accesso in stile Internet per un utente basato sullo standard Internet RFC 822. L'UPN è più breve di un nome distinto e più facile da ricordare. Per convenzione, deve eseguire il mapping al nome di posta elettronica dell'utente. Il punto dell'UPN consiste nel consolidare gli spazi dei nomi di posta elettronica e accesso in modo che l'utente debba solo ricordare un solo nome.

### <a name="upn-format"></a>Formato UPN

Un UPN è costituito da un prefisso UPN (il nome dell'account utente) e un suffisso UPN (nome di dominio DNS). Il prefisso viene unito al suffisso usando il simbolo \"\@\". Ad esempio, "someone@ example.com". Un UPN deve essere univoco tra tutti gli oggetti entità di sicurezza in una foresta di directory. Ciò significa che è possibile riutilizzare il prefisso di un UPN, non con lo stesso suffisso.

Un suffisso UPN presenta le restrizioni seguenti:

-   Deve corrispondere al nome DNS di un dominio, ma non deve necessariamente corrispondere al nome del dominio che contiene l'utente.
-   Deve corrispondere al nome di un dominio nella foresta di domini corrente o a un nome alternativo elencato nell'attributo **upnSuffixes** del contenitore di partizioni all'interno del contenitore di configurazione.

### <a name="upn-management"></a>Gestione UPN

Un UPN può essere assegnato, ma non è obbligatorio, quando viene creato un account utente. Quando viene creato un UPN, non è influenzato dalle modifiche apportate ad altri attributi dell'oggetto utente, ad esempio l'utente che viene rinominato o spostato. Ciò consente all'utente di memorizzare lo stesso nome di accesso se una directory viene ristrutturata. Tuttavia, un amministratore può modificare un UPN. Quando si crea un nuovo oggetto utente, è necessario controllare il dominio locale e il catalogo globale per il nome proposto per assicurarsi che non esista già.

Quando un utente utilizza un UPN per accedere a un dominio, l'UPN viene convalidato cercando il dominio locale e quindi il catalogo globale. Se il nome UPN non viene trovato nel catalogo globale, il tentativo di accesso ha esito negativo.

## <a name="objectguid"></a>objectGUID

L'attributo **objectGUID** è l'identificatore univoco di un utente. L'attributo è un identificatore univoco globale (GUID) a 128 bit a valore singolo e viene archiviato come struttura di [**stringa di \_ ottetto \_ ADS**](/windows/win32/api/iads/ns-iads-ads_octet_string) . Il GUID viene creato dal server Active Directory quando viene creato un oggetto utente.

Poiché il nome distinto di un oggetto viene modificato se l'oggetto viene rinominato o spostato, il nome distinto non è un identificatore attendibile di un oggetto. In Active Directory Domain Services, l'attributo **objectGUID** di un oggetto non viene mai modificato, anche se l'oggetto viene rinominato o spostato. È possibile recuperare il formato stringa di **objectGUID** usando il metodo della proprietà **GUID** nei [metodi della proprietà IADs](/windows/desktop/ADSI/iads-property-methods).

## <a name="samaccountname"></a>sAMAccountName

L'attributo **sAMAccountName** è un nome di accesso utilizzato per supportare client e server della versione precedente di Windows, ad esempio windows NT 4,0, Windows 95, Windows 98 e LAN Manager. Il nome di accesso deve essere composto da un massimo di 20 caratteri ed essere univoco tra tutti gli oggetti entità di sicurezza all'interno del dominio.

## <a name="objectsid"></a>objectSid

L'attributo **objectSID** è l'ID di sicurezza (SID) dell'utente. Il SID viene utilizzato dal sistema per identificare un utente e le relative appartenenze a gruppi durante le interazioni con la sicurezza di Windows. L'attributo è a valore singolo. Il SID è un valore binario univoco utilizzato per identificare l'utente come entità di sicurezza.

Il SID viene impostato dal sistema quando viene creato l'utente. Ogni utente dispone di un SID univoco emesso da un dominio di Windows e archiviato nell'attributo **objectSID** dell'oggetto utente nella directory. Ogni volta che un utente esegue l'accesso, il sistema Recupera il SID dell'utente dalla directory e lo inserisce nel token di accesso dell'utente. Il SID dell'utente viene usato anche per recuperare i SID per i gruppi di cui l'utente è membro e li inserisce nel token di accesso dell'utente. Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può essere usato di nuovo per identificare un altro utente o gruppo.

## <a name="sidhistory"></a>sIDHistory

L'attributo **sIDHistory** contiene i SID precedenti per l'oggetto utente. Si tratta di un attributo multivalore. Un oggetto utente dispone di SID precedenti se l'utente è stato spostato in un altro dominio. Ogni volta che un oggetto utente viene spostato in un nuovo dominio, viene creato un nuovo SID a cui viene assegnato l'attributo **objectSID** e il SID precedente viene aggiunto all'attributo **sIDHistory** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi dell'oggetto utente](user-object-attributes.md)
</dt> </dl>

 

 