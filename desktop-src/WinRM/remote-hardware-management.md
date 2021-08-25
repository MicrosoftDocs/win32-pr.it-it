---
title: Gestione hardware remota
description: Gestione hardware remota
ms.assetid: 0ea6d075-6154-4ab9-adcb-e599e5aee614
ms.tgt_platform: multiple
keywords:
- Gestione hardware remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db94c1f50b05f5180504ecef68bf10b1a5a596c9a9f88b96e7c5efb9faaa89bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858731"
---
# <a name="remote-hardware-management"></a>Gestione hardware remota

Windows La gestione hardware di Gestione remota è progettata per ridurre i costi di amministrazione IT complessivi fornendo il monitoraggio e il controllo dei componenti hardware remoti, soprattutto prima dell'avvio del sistema e dopo un errore del sistema operativo.

Original Equipment Manufacturers (OEM) ha sviluppato un'architettura comune per risolvere la necessità di gestione dell'hardware. Un aspetto importante di questa architettura è il [*baseboard management controller*](windows-remote-management-glossary.md) (BMC). Un BMC è un dispositivo specializzato che monitora lo stato del computer server. Il BMC fornisce il controllo remoto dell'hardware del server, recupera i dati sullo stato e riceve notifiche sugli errori critici e altre modifiche dello stato dell'hardware. Uno script o un'applicazione che monitora un server remoto può ottenere dati dal server [*in banda,*](windows-remote-management-glossary.md)tramite il sistema operativo remoto o [*fuori banda,*](windows-remote-management-glossary.md)direttamente dal BMC.

Un BMC dispone di sensori in grado di rilevare, ad esempio, quando il computer server si surriscalda o quando la tensione non è compreso nell'intervallo accettabile. Esistono diversi standard per definire l'architettura di BMC. [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) è uno standard di questo tipo usato di frequente. Tuttavia, nonostante lo standard IPMI, l'accesso di gestione all'hardware del server è proprietario e richiede l'uso di strumenti di gestione forniti dagli OEM. Inoltre, l'accesso remoto a un BMC viene fornito tramite un protocollo di collegamento specializzato, RMCP (Remote Management Control Protocol), che dispone di meccanismi di sicurezza non standard per l'autenticazione dell'accesso.

Il [provider MICROSOFT IPMI e](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) il driver IPMI consentono di ottenere dati BMC da computer server remoti tramite un provider WMI standard con [classi](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI . Sebbene sia possibile scrivere uno script WMI normale che ottiene dati remoti tramite DCOM, in molti casi il metodo preferito per ottenere i dati IPMI è tramite l'utilità della riga di comando **Winrm** o l'API di scripting [WinRM](winrm-scripting-api.md) o [WinRM C++.](winrm-c---api.md) L'utilità Winrm e le API del servizio Gestione remota Windows si basano sul protocollo WS-Management e possono ottenere dati IPMI da computer locali o remoti senza usare DCOM.

Il BMC include anche un database di eventi denominato Registro eventi di sistema (SEL) che registra gli eventi nel computer monitorato. Non è possibile sottoscrivere per il recapito di questi eventi a uno script come è possibile con le classi di eventi WMI. È tuttavia possibile usare lo strumento Wecutil.exe riga di comando per sottoscriverli. Per altre informazioni su come usare questo strumento, al prompt dei comandi digitare **wecutil /?**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protocollo WS-Management](ws-management-protocol.md)
</dt> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> </dl>

 

 