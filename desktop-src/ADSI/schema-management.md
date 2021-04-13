---
title: Gestione dello schema
description: Il componente provider di esempio ADSI definisce le classi dello schema \ 0034; unità organizzativa \ 0034; e \ 0034; Utente \ 0034; e gestisce queste classi dello schema nel modo seguente.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- Gestione dello schema ADSI
- gestione dello schema ADSI
- gestione degli schemi ADSI
- schemi, gestione di ADSI
- gestione di uno schema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104560752"
---
# <a name="schema-management"></a>Gestione dello schema

Il componente provider di esempio ADSI definisce le classi di schema "unità organizzativa" e "utente" e gestisce queste classi dello schema nel modo seguente.

La classe dello schema "unità organizzativa" è rappresentata da un oggetto contenitore ADs e può contenere altre "unità organizzative" e "utenti". L'oggetto contenitore supporta le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). La classe dello schema "User" è rappresentata da un oggetto Active Directory generico e non contiene altri tipi di oggetti. Nel componente provider di esempio, l'oggetto utente viene implementato come un oggetto Active Directory generico che supporta le interfacce **IUnknown**, **IDispatch** e **IADs**. Tenere presente che l'oggetto utente, in questo caso, non supporta l'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

Il componente provider di esempio deve implementare anche l'oggetto spazio dei nomi ADs, che supporta le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

Nella figura seguente vengono illustrati i dettagli dello schema che rappresenta le due classi dello schema dei componenti del provider di esempio.

![schema del componente provider di esempio ADSI](images/dssmsch.png)

Tenere presente che nella figura precedente la classe dello schema "unità organizzativa" definisce tre proprietà: "Description", "headcounts" e "ID". La classe dello schema "User" definisce quattro proprietà: "ID", "Name", "PhoneNumber" e "title". La proprietà "ID" è condivisa da entrambe le classi di schema. Ogni proprietà è definita dall'oggetto sintassi "String" o "Integer".

> [!Note]  
> Gli oggetti sintassi non sono presenti nella prima versione del componente provider di esempio. Tuttavia, nella maggior parte delle implementazioni dello schema di Microsoft ADSI, gli oggetti sintassi sono inclusi nell'oggetto contenitore dello schema, così come gli oggetti classe e proprietà dello schema. Per questo motivo, vengono visualizzati qui.

 

Questo componente del provider rende accessibili i dati dello schema all'applicazione client ADSI sotto forma di oggetti della classe ADs, oggetti proprietà ADs e oggetti sintassi ADs, tutti all'interno di un oggetto contenitore di classi di schema, in modo che i dati dello schema possano essere recuperati in fase di esecuzione.

ADsPaths per gli oggetti contenitore della classe dello schema definiti per il componente provider di esempio sono "Sample://Seattle/schema" e "Sample://Toronto/schema". In questo esempio, il contenuto degli schemi è identico.

 

 