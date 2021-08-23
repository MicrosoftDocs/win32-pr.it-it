---
title: Gestione dello schema
description: Il componente provider di esempio ADSI definisce le classi di schema \ 0034; unità organizzativa \ 0034; e \ 0034; Utente \ 0034; e gestiscono queste classi di schema nel modo seguente.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- ADSI per la gestione dello schema
- gestione dello schema ADSI
- gestione di schemi ADSI
- schemi, gestione di ADSI
- gestione di uno schema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddb8fcc3d29dce27ac2b74c9c8e79d1cef2f9d2a23307e9b7626861ed3e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770487"
---
# <a name="schema-management"></a>Gestione dello schema

Il componente provider di esempio ADSI definisce le classi di schema "Unità organizzativa" e "Utente" e gestisce queste classi di schema nel modo seguente.

La classe di schema "Unità organizzativa" è rappresentata da un oggetto contenitore ADs e può contenere altre "unità organizzative" e "utenti". L'oggetto contenitore supporta le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). La classe di schema "User" è rappresentata da un oggetto Active Directory generico e non contiene altri tipi di oggetti. Nel componente provider di esempio l'oggetto User viene implementato come oggetto Active Directory generico che supporta le interfacce **IUnknown**, **IDispatch** e **IADs**. Tenere presente che l'oggetto User, in questo caso, non supporta [**l'interfaccia IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser)

Il componente provider di esempio deve implementare anche l'oggetto spazio dei nomi ADs, che supporta le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

Nella figura seguente vengono illustrati i dettagli dello schema che rappresenta le due classi dello schema del componente del provider di esempio.

![Schema del componente del provider di esempio adsi](images/dssmsch.png)

Tenere presente che nella figura precedente la classe dello schema "Unità organizzativa" definisce tre proprietà: "Description", "Headcounts" e "ID". La classe di schema "User" definisce quattro proprietà: "ID", "Name", "PhoneNumber" e "Title". La proprietà "ID" è condivisa da entrambe le classi dello schema. Ogni proprietà è definita dall'oggetto sintassi "String" o "Integer".

> [!Note]  
> Gli oggetti sintassi non sono presenti nella prima versione del componente provider di esempio. Tuttavia, nella maggior parte delle implementazioni dello schema Microsoft ADSI, gli oggetti sintassi sono inclusi nell'oggetto contenitore dello schema, così come lo sono gli oggetti classe dello schema e proprietà. Per questo motivo, vengono visualizzati qui.

 

Questo componente del provider rende i dati dello schema accessibili all'applicazione client ADSI sotto forma di oggetti classe ADs, oggetti proprietà ADs e oggetti sintassi ADs, tutti all'interno di un oggetto contenitore della classe dello schema, in modo che i dati dello schema possano essere recuperati in fase di esecuzione.

Gli ADsPath per gli oggetti contenitore della classe dello schema definiti per il componente provider di esempio sono "Sample://Seattle/schema" e "Sample://Toronto/schema". In questo esempio il contenuto degli schemi è identico.

 

 