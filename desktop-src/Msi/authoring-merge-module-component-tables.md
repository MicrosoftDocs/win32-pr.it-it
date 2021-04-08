---
description: In ogni modulo merge è necessaria una tabella di componenti.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Creazione di tabelle di componenti del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049911"
---
# <a name="authoring-merge-module-component-tables"></a>Creazione di tabelle di componenti del modulo merge

In ogni modulo merge è necessaria una [tabella di componenti](component-table.md) . Questa tabella contiene un record per ogni componente fornito dal modulo merge al file con estensione msi di destinazione. Si noti che ogni componente deve essere specificato anche nella [tabella ModuleComponents](modulecomponents-table.md) descritta in creazione di [tabelle ModuleComponents](authoring-modulecomponents-tables.md).

Utilizzare la convenzione di denominazione standard quando si immettono i nomi nella colonna componente per assicurarsi che l'identificatore per ogni componente sia univoco per tutti i moduli unione e i database di installazione. Per ulteriori informazioni, vedere [denominazione delle chiavi primarie nei database dei moduli di merge](naming-primary-keys-in-merge-module-databases.md).

Completare i campi rimanenti in ogni record come descritto per un database di installazione nella [tabella dei componenti](component-table.md). I componenti aggiunti a un pacchetto da un modulo merge devono rispettare le linee guida per i componenti Windows Installer validi descritti nelle sezioni seguenti:

-   [Componenti Windows Installer](windows-installer-components.md)
-   [Organizzazione di applicazioni in componenti](organizing-applications-into-components.md)

 

 



