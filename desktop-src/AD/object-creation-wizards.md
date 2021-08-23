---
title: Creazioni guidate per la creazione di oggetti
description: Negli snap-in MMC amministrativi di Active Directory Domain Services l'utente può creare nuovi oggetti in una directory aprendo il menu di scelta rapida per il contenitore in cui verrà creato il nuovo oggetto, scegliendo Nuovo e scegliendo la classe di oggetto da creare. La creazione di nuove istanze di un oggetto avvia la Creazione guidata oggetto. Ogni classe di oggetto può specificare l'uso di una creazione guidata specifica oppure può usare una creazione guidata generica. Per le classi comuni, ad esempio user e organizationalUnit, lo snap-in Utenti e computer di Active Directory fornisce un set standard di creazioni guidate. Esistono due modi per estendere una creazione guidata Sostituire una procedura guidata esistente o specificarne una se non ne esiste una per la classe La procedura guidata esistente viene sostituita creando un'estensione per la creazione di oggetti primaria. Un'estensione di creazione primaria fornisce il primo set di pagine ed è ospitata come le pagine native. Un'estensione di creazione primaria supporta anche il meccanismo di estendibilità in modo che altre estensioni della creazione guidata possano essere richiamate. Per un esempio di estensione primaria, vedere l'esempio scpwizard in Platform Software Development Kit (SDK). Estendere una procedura guidata esistente Una procedura guidata esistente può essere estesa con un'estensione secondaria per la creazione di oggetti. Un'estensione di creazione secondaria aggiunge pagine della procedura guidata alle pagine native o all'estensione primaria. Per altre informazioni e un esempio di estensione di creazione secondaria, vedere l'esempio userwizard in Platform SDK.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- oggetti AD, procedure guidate di creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97c5c8f1b521d28c926d53830135dbb1b1fc907758e7047bc91c68856eedc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025588"
---
# <a name="object-creation-wizards"></a>Creazioni guidate per la creazione di oggetti

Negli snap-in MMC amministrativi di Active Directory Domain Services l'utente può creare nuovi oggetti in una directory aprendo il menu di scelta rapida per il contenitore in cui verrà creato il nuovo oggetto, scegliendo Nuovo e scegliendo la classe dell'oggetto da creare. La creazione di nuove istanze di un oggetto avvia la Creazione guidata oggetto. Ogni classe di oggetto può specificare l'uso di una creazione guidata specifica oppure può usare una creazione guidata generica. Per le classi comuni, ad esempio [**user**](/windows/desktop/ADSchema/c-user) e [**organizationalUnit,**](/windows/desktop/ADSchema/c-organizationalunit)lo snap-in Utenti e computer di Active Directory fornisce un set standard di creazioni guidate.

Esistono due modi per estendere una creazione guidata:

-   Sostituire una procedura guidata esistente o specificarne una se non ne esiste una per la classe: la procedura guidata esistente viene sostituita creando un'estensione per la creazione di *oggetti primaria.* Un'estensione di creazione primaria fornisce il primo set di pagine ed è ospitata come le pagine native. Un'estensione di creazione primaria supporta anche il meccanismo di estendibilità in modo che altre estensioni della creazione guidata possano essere richiamate. Per un esempio di estensione primaria, vedere l'esempio scpwizard in Platform Software Development Kit (SDK).
-   Estendere una procedura guidata esistente: una procedura guidata esistente può essere estesa con *un'estensione secondaria per la creazione di oggetti.* Un'estensione di creazione secondaria aggiunge pagine della procedura guidata alle pagine native o all'estensione primaria. Per altre informazioni e un esempio di estensione di creazione secondaria, vedere l'esempio userwizard in Platform SDK.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione presuppone che il lettore abbia familiarità con le operazioni COM e lo sviluppo di componenti con C++. Attualmente non è possibile creare un'estensione per la creazione guidata di oggetti di Active Directory usando Visual Basic.

## <a name="creating-an-active-directory-object-creation-extension"></a>Creazione di un'estensione per la creazione di oggetti di Active Directory

Le estensioni per la creazione di oggetti primaria e secondaria sono server COM in-process che implementano determinate interfacce e vengono registrate con Active Directory Domain Services.

**Per creare e installare un'estensione per la creazione di oggetti**

1.  Creare la DLL dell'estensione per la creazione di oggetti. Un'estensione per la creazione di oggetti è un server COM in-process che, come minimo, implementa l'interfaccia [**IDsAdminNewObjExt.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) Per altre informazioni, vedere [Implementazione dell'oggetto COM dell'estensione per la creazione di oggetti](implementing-the-object-creation-extension-com-object.md).
2.  Installare l'estensione di creazione nei computer in cui deve essere usata l'estensione di creazione. A tale scopo, creare un pacchetto di Microsoft Windows Installer per la DLL di creazione dell'estensione e distribuire il pacchetto in modo appropriato usando i criteri di gruppo. Per altre informazioni, vedere [Distribuzione di Interfaccia utente componenti](distributing-user-interface-components.md).
3.  Registrare l'estensione di creazione nel registro Windows e con Active Directory Domain Services. Per altre informazioni, vedere [Registrazione dell'estensione per la creazione di oggetti.](registering-the-object-creation-extension.md)

## <a name="using-an-object-creation-wizard"></a>Utilizzo della Creazione guidata oggetto

Una creazione guidata di oggetti può essere richiamata anche da un'applicazione diversa dagli snap-in MMC amministrativi di Active Directory Domain Services. Per altre informazioni, vedere [Richiamo di creazioni guidate dall'applicazione.](invoking-creation-wizards-from-your-application.md)

Se una creazione guidata non è registrata per una classe di oggetti, gli snap-in amministrativi forniscono una creazione guidata generica. La creazione guidata generica viene compilata in fase di esecuzione dall'elenco delle proprietà obbligatorie per la classe dell'oggetto creato. Per ogni proprietà obbligatoria, viene aggiunta una pagina all'interfaccia utente. La creazione guidata generica non è estendibile. Se è necessaria l'estendibilità, deve essere sostituita con un'estensione per la creazione di oggetti primaria.

 

 