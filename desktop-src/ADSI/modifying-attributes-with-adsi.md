---
title: Modifica degli attributi con ADSI
description: Per modificare i valori degli attributi, ADSI fornisce i metodi IADs. Put e IADs. PutEx. Questi metodi modificano i dati nella cache sul lato client. È necessario chiamare il metodo IADs. SetInfo per eseguire il commit delle modifiche nella directory.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modifica degli attributi con ADSI
- Attributi ADSI, modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399721"
---
# <a name="modifying-attributes-with-adsi"></a>Modifica degli attributi con ADSI

Per modificare i valori degli attributi, ADSI fornisce i metodi [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Questi metodi modificano i dati nella cache sul lato client. È necessario chiamare il metodo [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) per eseguire il commit delle modifiche nella directory.

> [!Note]  
> Quando si esegue il commit di più modifiche di attributo in una singola chiamata a [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), se non è possibile modificare un singolo attributo, nessuno degli attributi verrà modificato. Se, ad esempio, si modificano gli attributi [**sn**](/windows/desktop/ADSchema/a-sn) e [**given**](/windows/desktop/ADSchema/a-givenname) e si cancella l'attributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) di un oggetto utente senza alcuna chiamata successiva al metodo **seinfo** , le modifiche vengono immesse quando si chiama **seinfo**. Se una o più delle modifiche non sono consentite e pertanto non possono essere eseguite, nessuna delle modifiche collettive apportate agli attributi viene immessa durante la chiamata a **seinfo**.

 

Il metodo [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) accetta un nome di attributo e un parametro Variant. Utilizzare questo metodo per impostare attributi che contengono valori singoli e multipli.

Il metodo [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) fornisce il controllo sulle operazioni sugli attributi multivalore. È possibile accodare, eliminare, aggiornare e cancellare i valori esistenti. Il metodo **IADs. PutEx** prevede sempre una matrice Variant di valori di attributo. Tuttavia, è possibile usare questo metodo per impostare anche un attributo con un valore singolo.

Il metodo [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa le operazioni specificate dall'enumerazione [**\_ enum dell' \_ operazione \_ della proprietà ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .

 

 