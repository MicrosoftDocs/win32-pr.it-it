---
description: Per installare un file, un tipo di carattere o una chiave del registro di sistema in modo che non venga rimosso quando il prodotto viene disinstallato, l'intero componente contenente il file, il tipo di carattere o la chiave del registro di sistema deve essere reso permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058326"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema

Per installare un file, un tipo di carattere o una chiave del registro di sistema in modo che non venga rimosso quando il prodotto viene disinstallato, l'intero componente contenente il file, il tipo di carattere o la chiave del registro di sistema deve essere reso permanente. Per rendere permanente un componente, impostare **msidbComponentAttributesPermanent** nella colonna attributi della [tabella Component](component-table.md).

Si noti che il programma di installazione rimuove una chiave del registro di sistema dopo la rimozione dell'ultimo valore o della sottochiave sotto la chiave. Per evitare che una chiave del registro di sistema vuota venga rimossa durante la disinstallazione, scrivere un valore fittizio sotto la chiave necessaria e immettere + nella colonna nome della [tabella del registro di sistema](registry-table.md).

 

 



