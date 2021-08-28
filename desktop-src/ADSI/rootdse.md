---
title: RootDSE (ADSI)
description: Ogni server di directory ha una voce univoca denominata RootDSE. Fornisce dati sul server, ad esempio le relative funzionalità, la versione LDAP supportata e i contesti di denominazione utilizzati.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59176315339e7458f332e2226f880b79afa10c5afc2c5089295866f6bf93939c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770631"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Ogni server di directory ha una voce univoca denominata **RootDSE**. Fornisce dati sul server, ad esempio le relative funzionalità, la versione LDAP supportata e i contesti di denominazione utilizzati.

Ad esempio, per creare uno script o un'applicazione che può essere eseguita in qualsiasi Windows di dominio. È possibile specificare il nome distinto, il nome del server o il nome di dominio durante la connessione ad Active Directory. Se queste informazioni non sono disponibili, è possibile usare **l'oggetto RootDSE** per stabilire una connessione. Nell'esempio di codice seguente viene modificata la descrizione del dominio in qualsiasi dominio.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Ottenendo **l'attributo defaultNamingContext** da **RootDSE**, è possibile eseguire l'associazione al dominio corrente, ad esempio, fabrikam **defaultNamingContext** è DC=Fabrikam, DC=COM.

Per enumerare le proprietà di **RootDSE,** usare [**l'interfaccia IADsPropertyList.**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IDirectoryObject non**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) può essere usato per questa attività.

Per altre informazioni, vedere [Associazione serverless e RootDSE.](/windows/desktop/AD/serverless-binding-and-rootdse)

 

 