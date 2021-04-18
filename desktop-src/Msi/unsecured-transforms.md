---
description: Per impostazione predefinita, le trasformazioni che non sono state protette come descritto in trasformazioni protette sono trasformazioni non protette.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Trasformazioni non protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319416"
---
# <a name="unsecured-transforms"></a>Trasformazioni non protette

Per impostazione predefinita, le trasformazioni che non sono state protette come descritto in [trasformazioni protette](secured-transforms.md) sono trasformazioni non protette.

Per applicare una trasformazione non protetta durante l'installazione di un pacchetto, passare i nomi dei file di trasformazione nella proprietà [**TRANSforms**](transforms.md) o nella stringa della riga di comando. Non iniziare la stringa con i caratteri @ o \| o impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) . Si noti che non è possibile combinare trasformazioni non protette e [trasformazioni protette](secured-transforms.md) nello stesso elenco di trasformazioni.

Se il pacchetto viene installato o annunciato nel [contesto di installazione](installation-context.md)per utente e presenta trasformazioni non protette, il programma di installazione salva l'origine di trasformazione nella cartella Application Data nel profilo dell'utente. Questo consente a un utente di mantenere la personalizzazione di un prodotto durante il passaggio da un computer all'altra.

Se il pacchetto viene installato o annunciato nel [contesto di installazione](installation-context.md)per computer e utilizza trasformazioni non protette, il programma di installazione salva l'origine di trasformazione nella cartella% windir% \\ Installer.

Durante una prima installazione del pacchetto, il programma di installazione cerca innanzitutto la trasformazione nell'origine fornita dalla proprietà [**TRANSforms**](transforms.md) o dalla stringa della riga di comando. Se l'origine non è disponibile, il programma di installazione cerca la trasformazione in corrispondenza dell'origine del pacchetto accanto al file con estensione msi.

Durante un' [installazione di manutenzione](maintenance-installation.md), il programma di installazione cerca la trasformazione nel percorso della cache. Se la copia della trasformazione memorizzata nella cache non è più disponibile, il programma di installazione cerca la trasformazione in corrispondenza dell'origine del pacchetto accanto al file con estensione msi.

Per altre informazioni, vedere [applicazione di trasformazioni](applying-transforms.md) e [resilienza dell'origine](source-resiliency.md).

 

 



