---
title: Creazione guidata oggetto
description: Negli snap-in di MMC amministrativi di Active Directory Domain Services, l'utente può creare nuovi oggetti in una directory aprendo il menu di scelta rapida per il contenitore in cui verrà creato il nuovo oggetto, scegliendo nuovo e scegliendo la classe dell'oggetto da creare. La creazione di nuove istanze di un oggetto avvia la creazione guidata oggetto. Ogni classe di oggetti può specificare l'utilizzo di una procedura guidata di creazione specifica oppure può utilizzare una procedura guidata di creazione generica. Per le classi comuni, ad esempio User e organizationalUnit, lo snap-in Active Directory utenti e computer fornisce un set standard di creazioni guidate. Esistono due modi per estendere la creazione guidata di una procedura guidata esistente oppure specificarne uno se non esiste per la classe. la procedura guidata esistente viene sostituita dalla creazione di un'estensione per la creazione di oggetti primari. Un'estensione per la creazione primaria fornisce il primo set di pagine ed è ospitata in modo analogo alle pagine native. Un'estensione per la creazione primaria supporta inoltre il meccanismo di estendibilità, in modo che sia possibile richiamare altre estensioni della creazione guidata. Per un esempio di estensione primaria, vedere l'esempio scpwizard nel Software Development Kit (SDK) della piattaforma. Estendi una procedura guidata esistente è possibile estendere una procedura guidata esistente con un'estensione per la creazione di oggetti secondari. Un'estensione per la creazione secondaria aggiunge le pagine della procedura guidata alle pagine native o all'estensione primaria. Per ulteriori informazioni e un esempio di estensione per la creazione secondaria, vedere l'esempio userwizard in Platform SDK.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- oggetti AD, creazione guidata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc3dbacaf6eee5670fdacd9a587a497397c4d1b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117551"
---
# <a name="object-creation-wizards"></a>Creazione guidata oggetto

Negli snap-in di MMC amministrativi di Active Directory Domain Services, l'utente può creare nuovi oggetti in una directory aprendo il menu di scelta rapida per il contenitore in cui verrà creato il nuovo oggetto, scegliendo **nuovo** e scegliendo la classe dell'oggetto da creare. La creazione di nuove istanze di un oggetto avvia la creazione guidata oggetto. Ogni classe di oggetti può specificare l'utilizzo di una procedura guidata di creazione specifica oppure può utilizzare una procedura guidata di creazione generica. Per le classi comuni, ad esempio [**User**](/windows/desktop/ADSchema/c-user) e [**OrganizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit), lo snap-in Active Directory utenti e computer fornisce un set standard di creazioni guidate.

Esistono due modi per estendere una procedura guidata di creazione:

-   Sostituire una procedura guidata esistente o specificarne una se non ne esiste una per la classe: la procedura guidata esistente viene sostituita dalla creazione di un'estensione per la *creazione di oggetti primari*. Un'estensione per la creazione primaria fornisce il primo set di pagine ed è ospitata in modo analogo alle pagine native. Un'estensione per la creazione primaria supporta inoltre il meccanismo di estendibilità, in modo che sia possibile richiamare altre estensioni della creazione guidata. Per un esempio di estensione primaria, vedere l'esempio scpwizard nel Software Development Kit (SDK) della piattaforma.
-   Estendi una procedura guidata esistente: è possibile estendere una procedura guidata esistente con un'estensione per la *creazione di oggetti secondari*. Un'estensione per la creazione secondaria aggiunge le pagine della procedura guidata alle pagine native o all'estensione primaria. Per ulteriori informazioni e un esempio di estensione per la creazione secondaria, vedere l'esempio userwizard in Platform SDK.

## <a name="developer-audience"></a>Sviluppatori

In questa documentazione si presuppone che il lettore abbia familiarità con l'operazione COM e lo sviluppo di componenti con C++. Non è attualmente possibile creare un'estensione per la creazione guidata oggetto Active Directory utilizzando Visual Basic.

## <a name="creating-an-active-directory-object-creation-extension"></a>Creazione di un'estensione per la creazione di oggetti Active Directory

Le estensioni per la creazione di oggetti primari e secondari sono server COM in-process che implementano determinate interfacce e vengono registrate con Active Directory Domain Services.

**Per creare e installare un'estensione per la creazione di oggetti**

1.  Creare la DLL di estensione per la creazione di oggetti. Un'estensione per la creazione di oggetti è un server COM in-process che implementa come minimo l'interfaccia [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) . Per ulteriori informazioni, vedere [Implementing the Object Creation Extension com Object](implementing-the-object-creation-extension-com-object.md).
2.  Installare l'estensione per la creazione nei computer in cui deve essere utilizzata l'estensione per la creazione. A tale scopo, creare un pacchetto di Microsoft Windows Installer per la DLL di estensione per la creazione e distribuire il pacchetto in modo appropriato usando i criteri di gruppo. Per ulteriori informazioni, vedere la pagina relativa alla [distribuzione dei componenti dell'interfaccia utente](distributing-user-interface-components.md).
3.  Registrare l'estensione per la creazione nel registro di sistema di Windows e con Active Directory Domain Services. Per ulteriori informazioni, vedere [registrazione dell'estensione per la creazione di oggetti](registering-the-object-creation-extension.md).

## <a name="using-an-object-creation-wizard"></a>Utilizzo di una procedura guidata di creazione di oggetti

Una procedura guidata per la creazione di oggetti può essere richiamata anche da un'applicazione diversa dagli snap-in di MMC amministrativi del Active Directory Domain Services. Per ulteriori informazioni, vedere [richiamo di creazioni guidate dall'applicazione](invoking-creation-wizards-from-your-application.md).

Se una procedura guidata di creazione non è registrata per una classe di oggetti, gli snap-in amministrativi forniscono una procedura guidata di creazione generica. La procedura guidata di creazione generica viene compilata in fase di esecuzione dall'elenco delle proprietà obbligatorie per la classe dell'oggetto creato. Per ogni proprietà obbligatoria, viene aggiunta una pagina all'interfaccia utente. La procedura guidata di creazione generica non è estendibile. Se è necessaria l'estendibilità, è necessario sostituirla con un'estensione per la creazione di oggetti primaria.

 

 