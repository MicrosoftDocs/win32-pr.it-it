---
description: Il Windows Installer organizza un'installazione sui concetti di componenti e funzionalità.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Componenti e funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130294"
---
# <a name="components-and-features"></a>Componenti e funzionalità

Il Windows Installer organizza un'installazione sui concetti di componenti e funzionalità.

Una funzionalità fa parte della funzionalità totale dell'applicazione che un utente può decidere di installare in modo indipendente. Per ulteriori informazioni, vedere [Windows Installer funzionalità](windows-installer-features.md).

Un componente è una parte dell'applicazione o del prodotto da installare. Il programma di installazione installa sempre o rimuove un componente dal computer di un utente come elemento coerente. I componenti di solito sono nascosti all'utente. Quando un utente seleziona una funzionalità per l'installazione, il programma di installazione determina i componenti che devono essere installati per fornire tale funzionalità. Per ulteriori informazioni, vedere [Windows Installer Components](windows-installer-components.md).

Gli autori dei pacchetti di installazione devono decidere come dividere l'applicazione in funzionalità e componenti. La selezione delle funzionalità è determinata principalmente dalle funzionalità dell'applicazione dal punto di vista dell'utente. Poiché i componenti di solito devono essere condivisi tra le applicazioni o anche tra i prodotti, è consigliabile che gli autori seguano un metodo standard per la selezione dei componenti. Per altre informazioni, vedere [organizzazione di applicazioni in componenti](organizing-applications-into-components.md).

 

 



