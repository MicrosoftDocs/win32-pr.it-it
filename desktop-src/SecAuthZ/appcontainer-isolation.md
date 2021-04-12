---
description: L'isolamento è l'obiettivo principale di un ambiente di esecuzione AppContainer.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Isolamento AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fec44fd3d6eb9495370c42e52726ceb0f63806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232817"
---
# <a name="appcontainer-isolation"></a>Isolamento AppContainer

L'isolamento è l'obiettivo principale di un ambiente di esecuzione AppContainer. Isolando un'applicazione da risorse non necessarie e da altre applicazioni, le opportunità di manipolazione dannosa sono ridotte al minimo. Se si concede l'accesso in base al privilegio minimo, le applicazioni e gli utenti non possono accedere alle risorse oltre i rispettivi diritti. Il controllo dell'accesso alle risorse protegge il processo, il dispositivo e la rete.

La maggior parte delle vulnerabilità in Windows inizia con l'applicazione. Alcuni esempi comuni includono l'applicazione di una suddivisione del browser o l'invio di un documento errato a Internet Explorer, nonché l'utilizzo di plug-in, ad esempio Flash. Più queste applicazioni possono essere isolate in un AppContainer, più sicuro è il dispositivo e le risorse. Anche se viene sfruttata una vulnerabilità in un'app, l'app non può accedere alle risorse oltre a quelle concesse a AppContainer. Le app dannose non possono assumere il resto del computer.

## <a name="credential-isolation"></a>Isolamento delle credenziali

Gestione delle identità e delle credenziali, AppContainer impedisce l'uso delle credenziali utente per accedere alle risorse o accedere ad altri ambienti. L'ambiente AppContainer crea un identificatore che usa le identità combinate dell'utente e dell'applicazione, in modo che le credenziali siano univoche per ogni coppia utente/applicazione e che l'applicazione non possa rappresentare l'utente.

## <a name="device-isolation"></a>Isolamento dei dispositivi

Isolando l'applicazione dalle risorse del dispositivo, ad esempio i sensori passivi (fotocamera, microfono, GPS) e le pompe di denaro (3G/4G, Telefono telefonico), l'ambiente AppContainer impedisce all'applicazione di sfruttare in modo dannoso il dispositivo. Queste risorse sono bloccate per impostazione predefinita ed è possibile concedere l'accesso in base alle esigenze. In alcuni casi queste risorse sono ulteriormente protette da "broker". Alcune risorse, ad esempio la tastiera e il mouse, sono sempre disponibili per l'applicazione AppContainer e residente.

## <a name="file-isolation"></a>Isolamento file

Controllando l'accesso ai file e al registro di sistema, l'ambiente AppContainer impedisce all'applicazione di modificare i file che non dovrebbero esserlo. È possibile concedere l'accesso in lettura/scrittura a file persistenti e chiavi del registro di sistema specifici. L'accesso in sola lettura è meno limitato. Un'applicazione ha sempre accesso ai file residenti in memoria creati in modo specifico per tale AppContainer.

## <a name="network-isolation"></a>Isolamento della rete

Isolando l'applicazione dalle risorse di rete oltre a quelle allocate in modo specifico, AppContainer impedisce all'applicazione di fuggire dall'ambiente e di sfruttare le risorse di rete in modo dannoso. È possibile concedere l'accesso granulare per l'accesso a Internet, l'accesso alla Intranet e fungere da server.

## <a name="process-isolation"></a>Isolamento del processo

Il sandboxing degli oggetti del kernel dell'applicazione, l'ambiente AppContainer impedisce all'applicazione di influenzare o influenzato da altri processi dell'applicazione. In questo modo si impedisce a un'applicazione indipendente correttamente di danneggiare altri processi in caso di un'eccezione.

## <a name="window-isolation"></a>Isolamento finestra

Isolando l'applicazione da altre finestre, l'ambiente AppContainer impedisce che l'applicazione influisca sulle altre interfacce dell'applicazione.

 

 



