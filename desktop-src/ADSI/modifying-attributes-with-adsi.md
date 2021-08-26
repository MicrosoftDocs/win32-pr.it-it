---
title: Modifica degli attributi con ADSI
description: Per modificare i valori degli attributi, ADSI fornisce i metodi IADs.Put e IADs.PutEx. Questi metodi modificano i dati nella cache sul lato client. Il metodo IADs.SetInfo deve essere chiamato per eseguire il commit delle modifiche nella directory.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modifica degli attributi con ADSI
- Attributi ADSI, modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef82d6a3d4c486fcd1fca1f5cba7ae62f57e66e713ed84551a5a9372cdc86683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079961"
---
# <a name="modifying-attributes-with-adsi"></a>Modifica degli attributi con ADSI

Per modificare i valori degli attributi, ADSI fornisce [**i metodi IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs.PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Questi metodi modificano i dati nella cache sul lato client. Il [**metodo IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) deve essere chiamato per eseguire il commit delle modifiche nella directory.

> [!Note]  
> Quando viene eseguito il commit di più modifiche dell'attributo in una singola chiamata a [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), se non è possibile modificare un singolo attributo, nessuno degli attributi verrà modificato. Ad esempio, se si modificano gli attributi [**sn**](/windows/desktop/ADSchema/a-sn) e [**givenName**](/windows/desktop/ADSchema/a-givenname) e si cancella l'attributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) di un oggetto utente senza chiamate successive al metodo **SetInfo,** le modifiche vengono immesse quando si chiama **SetInfo**. Se una o più modifiche non sono consentite e pertanto non possono essere eseguite, nessuna delle modifiche collettive apportate agli attributi viene immessa durante la chiamata a **SetInfo**.

 

Il [**metodo IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) accetta un nome di attributo e un parametro variant. Usare questo metodo per impostare attributi che contengono valori singoli e multipli.

Il [**metodo IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) fornisce il controllo sulle operazioni sugli attributi multivalore. È possibile aggiungere, eliminare, aggiornare e cancellare i valori esistenti. Il **metodo IADs.PutEx** prevede sempre una matrice variant di valori di attributo. Tuttavia, è possibile usare questo metodo per impostare anche un attributo con un singolo valore.

Il [**metodo IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa le operazioni specificate dall'enumerazione [**ADS PROPERTY OPERATION \_ \_ \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)

 

 