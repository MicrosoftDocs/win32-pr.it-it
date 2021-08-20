---
title: Linee guida generali per la programmazione
description: Linee guida per lo sviluppo di applicazioni in Servizi Desktop remoto ambiente.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b0e83daa98f59390408fa43f5c5f83ff547e3d0cad665d29922f4244913361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353882"
---
# <a name="general-programming-guidelines"></a>Linee guida generali per la programmazione

Le sezioni seguenti forniscono linee guida generali per lo sviluppo di applicazioni in Servizi Desktop remoto ambiente.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Livello di compatibilità delle applicazioni](application-compatibility-layer.md)
</dt> <dd>

Per eseguire applicazioni legacy in un ambiente Servizi Desktop remoto è possibile usare il Servizi Desktop remoto di compatibilità delle applicazioni.

</dd> <dt>

[Linee guida per le applicazioni client/server](client-server-application-guidelines.md)
</dt> <dd>

Le applicazioni client/server non devono presupporre che una connessione a un singolo computer sia equivalente a una singola sessione utente.

</dd> <dt>

[Monitoraggio delle connessioni e delle disconnessioni delle sessioni](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Per registrare un'applicazione Servizi Desktop remoto, archiviare il nome dell'applicazione server del canale virtuale nel Registro di sistema aggiungendo una sottochiave.

</dd> <dt>

[Linee guida per l'hardware delle periferiche](peripheral-hardware-guidelines.md)
</dt> <dd>

Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono assicurarsi che il software del driver di dispositivo forza la disabilitazione del reindirizzamento del dispositivo tramite criteri di sistema o criteri di gruppo.

</dd> <dt>

[Collegamento in fase di esecuzione a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

L'applicazione può usare l'API Servizi Desktop remoto per il collegamento dinamico al Wtsapi32.dll in fase di esecuzione. A tale scopo, l'applicazione deve chiamare la [**funzione LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Wtsapi32.dll.

</dd> </dl>

 

 