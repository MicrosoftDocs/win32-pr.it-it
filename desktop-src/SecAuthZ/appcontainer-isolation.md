---
description: L'isolamento è l'obiettivo principale di un ambiente di esecuzione AppContainer.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Isolamento di AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe42b12698983bc3a90af06be2bb45992013b52e16e6f7de37083d6c92b9422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784707"
---
# <a name="appcontainer-isolation"></a>Isolamento di AppContainer

L'isolamento è l'obiettivo principale di un ambiente di esecuzione AppContainer. Isolando un'applicazione da risorse non necessarie e altre applicazioni, le opportunità di manipolazione dannosa sono ridotte al minimo. La concessione dell'accesso in base ai privilegi minimi impedisce alle applicazioni e agli utenti di accedere alle risorse oltre i propri diritti. Il controllo dell'accesso alle risorse protegge il processo, il dispositivo e la rete.

La maggior parte delle vulnerabilità Windows l'applicazione. Alcuni esempi comuni includono l'interruzione di un'applicazione dal browser o l'invio di un documento non Internet Explorer e lo sfruttamento di plug-in, ad esempio flash. Più queste applicazioni possono essere isolate in un AppContainer, maggiore è la sicurezza del dispositivo e delle risorse. Anche se viene sfruttata la vulnerabilità in un'app, l'app non può accedere alle risorse oltre a quanto concesso a AppContainer. Le app dannose non possono assumere il controllo del resto del computer.

## <a name="credential-isolation"></a>Isolamento delle credenziali

Gestione dell'identità e delle credenziali, AppContainer impedisce l'uso delle credenziali utente per accedere alle risorse o accedere ad altri ambienti. L'ambiente AppContainer crea un identificatore che usa le identità combinate dell'utente e dell'applicazione, in modo che le credenziali siano univoche per ogni coppia utente/applicazione e che l'applicazione non possa rappresentare l'utente.

## <a name="device-isolation"></a>Isolamento del dispositivo

Isolando l'applicazione dalle risorse del dispositivo, ad esempio sensori passivi (fotocamera, microfono, GPS) e money pump (3G/4G, telefono dial), l'ambiente AppContainer impedisce all'applicazione di sfruttare il dispositivo in modo dannoso. Queste risorse sono bloccate per impostazione predefinita e possono essere concesse l'accesso in base alle esigenze. In alcuni casi queste risorse sono ulteriormente protette dai "broker". Alcune risorse, ad esempio tastiera e mouse, sono sempre disponibili per AppContainer e per l'applicazione residente.

## <a name="file-isolation"></a>Isolamento dei file

Controllando l'accesso a file e registro, l'ambiente AppContainer impedisce all'applicazione di modificare i file che non dovrebbero essere. L'accesso in lettura/scrittura può essere concesso a specifici file persistenti e chiavi del Registro di sistema. L'accesso in sola lettura è meno limitato. Un'applicazione ha sempre accesso ai file residenti in memoria creati in modo specifico per l'AppContainer.

## <a name="network-isolation"></a>Isolamento della rete

Isolando l'applicazione dalle risorse di rete oltre a quelle allocate in modo specifico, AppContainer impedisce all'applicazione di "evitare" l'ambiente e di sfruttare in modo dannoso le risorse di rete. È possibile concedere l'accesso granulare per l'accesso a Internet, l'accesso Intranet e fungere da server.

## <a name="process-isolation"></a>Isolamento del processo

La creazione di sandbox degli oggetti kernel dell'applicazione, l'ambiente AppContainer impedisce all'applicazione di influenzare o influenzare altri processi dell'applicazione. Ciò impedisce a un'applicazione contenuta correttamente di danneggiare altri processi in caso di eccezione.

## <a name="window-isolation"></a>Isolamento della finestra

Isolando l'applicazione da altre finestre, l'ambiente AppContainer impedisce all'applicazione di influire sulle altre interfacce dell'applicazione.

 

 



