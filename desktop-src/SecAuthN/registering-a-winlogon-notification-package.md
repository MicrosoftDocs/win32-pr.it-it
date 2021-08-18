---
description: Le informazioni sui pacchetti di notifica Winlogon vengono archiviate nel Registro di sistema. Le voci del Registro di sistema specificano il nome del pacchetto di notifica, il nome della DLL che implementa il pacchetto e i nomi delle funzioni che gestiscono gli eventi Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrazione di un pacchetto di notifica Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa41948062458581d607b64432166b99ba4701865a3c7b593365c87342359ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919670"
---
# <a name="registering-a-winlogon-notification-package"></a>Registrazione di un pacchetto di notifica Winlogon

Le informazioni [*sui pacchetti di notifica Winlogon*](../secgloss/w-gly.md) vengono archiviate nel Registro di sistema. Le voci del Registro di sistema specificano il nome del pacchetto di notifica, il nome della DLL che implementa il pacchetto e i nomi delle funzioni che gestiscono gli eventi Winlogon.

All'avvio di Winlogon, controlla il Registro di sistema e carica tutti i pacchetti di notifica registrati. Quando si verifica un evento, Winlogon chiama la funzione del gestore eventi designata per ogni pacchetto. In un sistema possono essere registrati più pacchetti di notifica degli eventi.

Per registrare il pacchetto di notifica, creare una chiave del Registro di sistema denominata **Notify** come sottochiave della chiave del Registro di sistema seguente e aggiungere i valori dettagliati in Voci del Registro [di sistema](registry-entries.md).

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
