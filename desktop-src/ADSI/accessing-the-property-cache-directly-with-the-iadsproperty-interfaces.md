---
title: Accesso alla cache delle proprietà con le interfacce IADsProperty
description: Le interfacce IADsProperty sono costituite da IADsPropertyList, IADsPropertyEntry e IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Accesso alla cache delle proprietà direttamente con le interfacce IADsProperty ADSI
- ADSI cache proprietà
- ADSI cache proprietà, uso delle interfacce IADsProperty per accedere alla cache delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/04/2019
ms.locfileid: "103956099"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Accesso alla cache delle proprietà con le interfacce IADsProperty

Le interfacce [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) sono costituite da [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue). Queste interfacce forniscono metodi per accedere direttamente e modificare le proprietà di una cache di oggetti. Una proprietà è nota come voce di proprietà e corrisponde a un attributo definito nello schema. Una voce di proprietà può contenere uno o molti valori di proprietà. Un set di voci di proprietà è organizzato come elenco delle proprietà.

L'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) gestisce l'elenco delle proprietà di un oggetto ADSI. L'interfaccia [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) esegue questa operazione per una voce di proprietà. Analogamente, l'interfaccia [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) rappresenta uno o più valori di proprietà. Insieme, forniscono un meccanismo per consentire agli utenti di:

-   Lavorare direttamente con la cache delle proprietà.
-   Utilizzare le directory che non contengono schemi, ad esempio un server LDAP versione 2.

Le interfacce [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* operano esclusivamente nella cache delle proprietà e non eseguono alcun tentativo di collaborazione con il server per recuperare o modificare i dati nell'archivio permanente. Queste interfacce vengono usate solo per esaminare e modificare le proprietà nella cache del client. Prima di usare queste interfacce, è necessario chiamare il metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o il metodo [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) in modo esplicito per caricare le proprietà dell'oggetto nella cache, se la cache non è stata inizializzata. Dopo la chiamata dei metodi di queste interfacce, è necessario chiamare [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) per salvare in modo permanente le modifiche apportate all'archivio directory sottostante.

Per altre informazioni e un esempio di codice che può essere usato per implementare queste interfacce, vedere [il codice di esempio per l'uso delle interfacce IADsProperty per accedere alla cache delle proprietà](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).

 

 




