---
description: Poiché un pacchetto di installazione può contenere i file che costituiscono un'applicazione e le informazioni necessarie per l'installazione, è possibile usare Windows Installer per aggiornare l'applicazione.
ms.assetid: da946739-9efc-4bf0-8a9a-6f6ead3c4a34
title: Applicazione di patch e aggiornamenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cee185461ac14c8eac336a5af0c1315eb5e027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967552"
---
# <a name="patching-and-upgrades"></a>Applicazione di patch e aggiornamenti

Poiché un pacchetto di installazione può contenere i file che costituiscono un'applicazione e le informazioni necessarie per l'installazione, è possibile usare Windows Installer per aggiornare l'applicazione. Il programma di installazione può aggiornare le informazioni nelle parti seguenti del pacchetto di installazione:

-   Il file con estensione msi.
-   File dell'applicazione.
-   Informazioni di registrazione del Windows Installer.

Il tipo di aggiornamento può essere caratterizzato dalle modifiche apportate dall'aggiornamento al codice del prodotto, alla versione del prodotto e al codice del pacchetto dell'applicazione. La versione del prodotto dell'applicazione è archiviata nella proprietà [**ProductVersion**](productversion.md) . Il codice del prodotto dell'applicazione è archiviato nella proprietà [**ProductCode**](productcode.md) . Il codice del [pacchetto](package-codes.md) dell'applicazione viene archiviato nella proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) .

Per modificare il [**ProductCode**](productcode.md) dell'applicazione, è necessario un aggiornamento che modifichi l'applicazione in un altro prodotto. Per ulteriori informazioni sugli aggiornamenti che richiedono la modifica del **ProductCode** , vedere [modifica del codice del prodotto](changing-the-product-code.md). L'aggiornamento può modificare il [**ProductVersion**](productversion.md) e lasciare invariato il **ProductCode** se le versioni future dell'applicazione dovranno distinguere tra le versioni aggiornate e non aggiornate del prodotto corrente. Il [codice del pacchetto](package-codes.md) identifica in modo univoco il pacchetto di installazione e deve essere sempre modificato ogni volta che l'aggiornamento o l'aggiornamento modifica tutte le informazioni nel pacchetto di installazione.

Quando si decide se modificare la versione del prodotto, è necessario considerare se le versioni future dell'applicazione dovranno distinguere tra le versioni aggiornate e non aggiornate del prodotto corrente. Per garantire una differenziazione in futuro, è consigliabile usare un [aggiornamento secondario](minor-upgrades.md) anziché un [piccolo aggiornamento](small-updates.md).

-   Se un aggiornamento modifica il file con estensione msi e i file dell'applicazione, ma non modifica la proprietà [**ProductCode**](productcode.md) o la proprietà [**ProductVersion**](productversion.md) , viene definito un [piccolo aggiornamento](small-updates.md).
-   Se l'aggiornamento modifica il valore di [**ProductVersion**](productversion.md), ma non modifica il [**ProductCode**](productcode.md), viene definito un [aggiornamento secondario](minor-upgrades.md).
-   Se l'aggiornamento modifica l'installazione in un prodotto completamente diverso, il [**ProductCode**](productcode.md) deve essere modificato e l'aggiornamento viene definito come [aggiornamento principale](major-upgrades.md).

> [!Note]  
> Per garantire la differenziazione delle versioni del prodotto corrente in futuro, è consigliabile usare un [aggiornamento secondario](minor-upgrades.md) anziché un aggiornamento di [piccole dimensioni](small-updates.md).

 

Nella tabella seguente vengono riepilogati i diversi tipi di aggiornamenti.



| Tipo di aggiornamento                       | ProductCode | ProductVersion | Descrizione                                                                                                                                                                                                                                                                                                           |
|--------------------------------------|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aggiornamento ridotto](small-updates.md)    | Nessuna modifica   | Nessuna modifica      | Aggiornamento di uno o due file troppo piccolo per garantire la modifica di [**ProductVersion**](productversion.md). Il codice del pacchetto nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) cambia. Può essere spedito come pacchetto di installazione completo o come [pacchetto di patch](patch-packages.md). |
| [Aggiornamento secondario](minor-upgrades.md)  | Nessuna modifica   | Modificato        | Un piccolo aggiornamento che rende le modifiche sufficientemente significative per giustificare la modifica della proprietà [**ProductVersion**](productversion.md) . Può essere spedito come pacchetto di installazione completo o come [pacchetto di patch](patch-packages.md).                                                                                                |
| [Aggiornamenti principali](major-upgrades.md) | Modificato     | Modificato        | Aggiornamento completo del prodotto che garantisce una modifica nella proprietà [**ProductCode**](productcode.md) . Fornito come [pacchetto di patch](patch-packages.md) o come pacchetto di installazione completo del prodotto.                                                                                                             |



 

> [!Note]  
> Il Windows Installer può installare un'applicazione o un aggiornamento per tutti gli utenti di un computer (contesto per computer) o per un particolare utente (contesto per utente), a seconda dei privilegi di accesso dell'utente, del valore della proprietà [**ALLUSERS**](allusers.md) e della versione del sistema operativo. Gli sviluppatori di applicazioni devono considerare in che modo verranno installati gli aggiornamenti del contesto. Se i contesti dell'applicazione e dell'aggiornamento sono diversi, è possibile che l'applicazione non venga aggiornata come previsto.

 

Gli utenti possono eseguire l'aggiornamento a un'applicazione reinstallando un pacchetto di Windows Installer per l'applicazione. Si noti che gli [aggiornamenti secondari](minor-upgrades.md) possono essere applicati in modo analogo ai [piccoli aggiornamenti](small-updates.md). Per ulteriori informazioni sull'aggiornamento di un'applicazione tramite la reinstallazione dell'applicazione, vedere le sezioni seguenti:

-   [Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md)
-   [Applicazione degli aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md)

Un aggiornamento a un'applicazione può essere fornito agli utenti come pacchetto di patch Windows Installer. Una patch può contenere un intero file o solo i bit di file necessari per aggiornare una parte di un file. Ciò significa che l'utente può scaricare una patch di aggiornamento che è molto più piccola dell'intero prodotto e che conserva le personalizzazioni degli utenti durante l'aggiornamento. Si noti che gli [aggiornamenti secondari](minor-upgrades.md) possono essere applicati in modo analogo ai [piccoli aggiornamenti](small-updates.md). Per ulteriori informazioni sull'aggiornamento di un'applicazione mediante una patch, vedere le sezioni seguenti:

-   [Patch](patching.md)
-   [Creazione di una patch di aggiornamento di piccole dimensioni](creating-a-small-update-patch.md)
-   [Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)
-   [Applicazione degli aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)

 

 



