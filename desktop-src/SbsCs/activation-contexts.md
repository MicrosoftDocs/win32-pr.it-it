---
description: I contesti di attivazione sono strutture di dati in memoria contenenti informazioni che il sistema può usare per reindirizzare un'applicazione per caricare una determinata versione della DLL, un'istanza dell'oggetto COM o una versione di finestra personalizzata.
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: Contesti di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21aaf2c4d2e4fc0f3ef691406e663dc5efac44a9d0b34880596d21cac8a5f621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142544"
---
# <a name="activation-contexts"></a>Contesti di attivazione

[*I contesti di*](a-sbscs-gly.md) attivazione sono strutture di dati in memoria contenenti informazioni che il sistema può usare per reindirizzare un'applicazione per caricare una determinata versione della DLL, un'istanza dell'oggetto COM o una versione di finestra personalizzata. Una sezione del contesto di attivazione può contenere informazioni di reindirizzamento DLL usate dal caricatore DLL. un'altra sezione può contenere informazioni sul server COM. Le funzioni del contesto di attivazione usano, creano, attivano e disattivano i contesti di attivazione. Le funzioni di attivazione possono reindirizzare l'associazione di un'applicazione a oggetti con nome di versione che specificano versioni specifiche di DLL, classi finestra, server COM, librerie dei tipi e interfacce. Per altre informazioni sulle funzioni e sulle strutture del contesto di attivazione, vedere Informazioni [di riferimento sul contesto di attivazione](activation-context-reference.md).

A partire da Windows XP, le funzioni del contesto di attivazione Windows usare le informazioni nei [manifesti](manifests.md) per creare oggetti con nome della versione. Se un'applicazione crea un processo chiamando [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), Windows verifica l'esistenza di un manifesto [dell'applicazione.](application-manifests.md) Se esiste un manifesto, Windows le informazioni nel manifesto per popolare il contesto di attivazione. Poiché i manifesti descrivono la dipendenza di un'applicazione dalle versioni [side-by-side](about-side-by-side-assemblies-.md) degli assembly, gli oggetti specificati senza versioni nel manifesto vengono mappati a oggetti con nome della versione. Ad esempio, il manifesto può descrivere DLL, file, classi finestra, server COM, librerie dei tipi e interfacce.

Quando viene creato un oggetto globale nel contesto di attivazione, il sistema assegna automaticamente all'oggetto un nome specifico della versione consultando il manifesto. Quando l'applicazione viene eseguita e richiede un oggetto denominato, ottiene l'oggetto denominato dalla versione. Ciò consente l'esecuzione di più versioni di un modulo di codice nel sistema contemporaneamente senza interferire tra loro. Ad esempio, [Windows Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) usa un manifesto per descrivere una dipendenza dalla versione 6.0 di COMCTL32 e per creare versioni delle classi finestra.

Se un'applicazione crea una risorsa chiamando [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), il processo specifica un nome di classe per tale funzione. La chiamata a [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) ottiene il contesto di attivazione corrente e verifica se esiste un mapping per il nome di classe specificato. Se esiste un mapping, userà tale versione del processo chiamante per risolvere il mapping e fornire il nome di classe specifico della versione. Windows una finestra con la routine della finestra, gli stili e altri attributi associati al nome e alla versione della classe.

Il contesto di attivazione viene gestito dal sistema nella maggior parte dei casi. Gli sviluppatori di applicazioni e i provider di assembly in genere non devono effettuare chiamate nello stack. Le applicazioni possono gestire un contesto di attivazione chiamando direttamente il contesto di attivazione. Per altre informazioni, vedere [Uso dell'API del contesto di attivazione](using-the-activation-context-api.md).

 

 
