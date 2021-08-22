---
description: Le trasformazioni che non sono state protette come descritto in Trasformazioni protette sono trasformazioni non protette per impostazione predefinita.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Trasformazioni non protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bb234a0cdee852d3a5e1717642f5325283a571b740c9d7b4a5f6901afb52c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499611"
---
# <a name="unsecured-transforms"></a>Trasformazioni non protette

Le trasformazioni che non sono state protette come descritto in [Trasformazioni](secured-transforms.md) protette sono trasformazioni non protette per impostazione predefinita.

Per applicare una trasformazione non protetta durante l'installazione di un pacchetto, passare i nomi dei file di trasformazione nella proprietà [**TRANSFORMS**](transforms.md) o nella stringa della riga di comando. Non iniziare la stringa con i caratteri @ o \| o impostare il criterio [TransformsSecure](transformssecure-policy.md) o [**la proprietà TRANSFORMSSECURE.**](transformssecure.md) Si noti che non è possibile combinare trasformazioni non protette e [trasformazioni protette](secured-transforms.md) nello stesso elenco di trasformazioni.

Se il pacchetto è installato o annunciato [](installation-context.md)nel contesto di installazione per utente e dispone di trasformazioni non protette, il programma di installazione salva l'origine della trasformazione nella cartella Dati applicazione nel profilo dell'utente. Ciò consente a un utente di mantenere la personalizzazione di un prodotto durante lo spostamento da un computer all'altro.

Se il pacchetto è installato o annunciato [](installation-context.md)nel contesto di installazione per computer e usa trasformazioni non protette, il programma di installazione salva l'origine della trasformazione nella cartella %windir% \\ Installer.

Durante la prima installazione del pacchetto, il programma di installazione cerca innanzitutto la trasformazione nell'origine fornita dalla proprietà [**TRANSFORMS**](transforms.md) o dalla stringa della riga di comando. Se questa origine non è disponibile, il programma di installazione cerca la trasformazione nell'origine del pacchetto accanto al file .msi file.

Durante [un'installazione di manutenzione,](maintenance-installation.md)il programma di installazione cerca la trasformazione nel percorso della cache. Se la copia memorizzata nella cache della trasformazione non è più disponibile, il programma di installazione cerca la trasformazione nell'origine del pacchetto accanto al file .msi file.

Per altre informazioni, vedere [Applicazione di trasformazioni e](applying-transforms.md) [resilienza dell'origine.](source-resiliency.md)

 

 



