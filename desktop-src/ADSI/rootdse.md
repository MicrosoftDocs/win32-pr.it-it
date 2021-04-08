---
title: RootDSE (ADSI)
description: Ogni server di directory dispone di una voce univoca denominata RootDSE. Fornisce dati sul server, ad esempio le funzionalità, la versione LDAP supportata e i contesti di denominazione utilizzati.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730242"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Ogni server di directory dispone di una voce univoca denominata **RootDSE**. Fornisce dati sul server, ad esempio le funzionalità, la versione LDAP supportata e i contesti di denominazione utilizzati.

Ad esempio, per creare uno script, o un'applicazione, che può essere eseguito in qualsiasi ambiente di dominio Windows. È possibile specificare il nome distinto, il nome del server o il nome di dominio quando ci si connette a Active Directory. Se non si dispone di queste informazioni, è possibile utilizzare l'oggetto **RootDSE** per stabilire una connessione. Nell'esempio di codice seguente viene modificata la descrizione del dominio in qualsiasi dominio.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Ottenendo l'attributo **defaultNamingContext** da **RootDSE**, è possibile eseguire l'associazione al dominio corrente. ad esempio, Fabrikam **defaultNamingContext** è DC = Fabrikam, DC = com.

Per enumerare le proprietà di **RootDSE**, usare l'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . Non è possibile usare [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per questa attività.

Per ulteriori informazioni, vedere [binding senza server e RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).

 

 