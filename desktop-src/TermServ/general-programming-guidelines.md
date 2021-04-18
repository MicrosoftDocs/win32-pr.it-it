---
title: Linee guida generali per la programmazione
description: Linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300024"
---
# <a name="general-programming-guidelines"></a>Linee guida generali per la programmazione

Nelle sezioni seguenti vengono fornite linee guida generali per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Livello di compatibilità delle applicazioni](application-compatibility-layer.md)
</dt> <dd>

Per eseguire applicazioni legacy in un ambiente Servizi Desktop remoto è possibile usare il Servizi Desktop remoto livello di compatibilità delle applicazioni.

</dd> <dt>

[Linee guida per applicazioni client/server](client-server-application-guidelines.md)
</dt> <dd>

Le applicazioni client/server non devono presupporre che una connessione a computer singolo sia equivalente a una singola sessione utente.

</dd> <dt>

[Monitoraggio di connessioni e disconnessioni di sessione](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Per registrare un'applicazione con Servizi Desktop remoto, archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave.

</dd> <dt>

[Linee guida hardware periferiche](peripheral-hardware-guidelines.md)
</dt> <dd>

Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono garantire che il software dei driver di dispositivo forzi la disabilitazione del reindirizzamento del dispositivo usando criteri di sistema o criteri di gruppo.

</dd> <dt>

[Collegamento di run-time a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

L'applicazione può usare l'API Servizi Desktop remoto per collegare in modo dinamico al Wtsapi32.dll in fase di esecuzione. A tale scopo, l'applicazione deve chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Wtsapi32.dll.

</dd> </dl>

 

 