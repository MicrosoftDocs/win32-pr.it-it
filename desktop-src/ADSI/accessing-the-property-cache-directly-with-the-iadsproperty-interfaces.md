---
title: Accesso alla cache delle proprietà con interfacce IADsProperty
description: Le interfacce IADsProperty sono costituite da IADsPropertyList, IADsPropertyEntry e IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Accesso diretto alla cache delle proprietà con le interfacce IADsProperty ADSI
- cache delle proprietà ADSI
- cache delle proprietà ADSI, uso delle interfacce IADsProperty per accedere alla cache delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a68cd77a10d6631b52e48ed19650dd5cd18dff0ee59ba2332db73b7fce1a8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024119"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Accesso alla cache delle proprietà con interfacce IADsProperty

Le [**interfacce IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) sono costituite da [**IADsPropertyList,**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue.**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) Queste interfacce forniscono metodi per accedere e modificare direttamente le proprietà di una cache di oggetti. Una proprietà è nota come voce di proprietà e corrisponde a un attributo definito nello schema. Una voce di proprietà può avere uno o più valori di proprietà. Un set di voci di proprietà è organizzato come elenco di proprietà.

[**L'interfaccia IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) gestisce l'elenco delle proprietà di un oggetto ADSI. [**L'interfaccia IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) esegue questa operazione per una voce di proprietà. Analogamente, [**l'interfaccia IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) rappresenta uno o più valori di proprietà. Insieme, forniscono un meccanismo che consente agli utenti di:

-   Usare direttamente la cache delle proprietà.
-   Usare directory che non contengono schemi, ad esempio un server LDAP versione 2.

Le [**interfacce IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) operano esclusivamente nella cache delle proprietà e non tentano di collaborare con il server per recuperare o modificare i dati \* nell'archivio permanente. Di conseguenza, queste interfacce vengono usate solo per esaminare e modificare le proprietà nella cache del client. Prima di usare queste interfacce, è necessario chiamare il metodo [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o il metodo [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) in modo esplicito per caricare le proprietà dell'oggetto nella cache, se la cache non è stata inizializzata. Dopo aver chiamato i metodi di queste interfacce, è necessario chiamare [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) per rendere persistenti le modifiche nell'archivio directory sottostante.

Per altre informazioni e un esempio di codice che può essere usato per implementare queste interfacce, vedere Codice di esempio per l'uso di [interfacce IADsProperty](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md)per accedere alla cache delle proprietà.

 

 




