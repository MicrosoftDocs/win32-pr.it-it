---
description: Per installare un file, un tipo di carattere o una chiave del Registro di sistema in modo che non venga rimosso quando il prodotto viene disinstallato, l'intero componente contenente il file, il tipo di carattere o la chiave del Registro di sistema deve essere reso permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Installazione di componenti permanenti, file, tipi di carattere, chiavi del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87818c2b9a80d582992dd964daa632575f51e5fa24f17a97af0191277e880df6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105101"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Installazione di componenti permanenti, file, tipi di carattere, chiavi del Registro di sistema

Per installare un file, un tipo di carattere o una chiave del Registro di sistema in modo che non venga rimosso quando il prodotto viene disinstallato, l'intero componente contenente il file, il tipo di carattere o la chiave del Registro di sistema deve essere reso permanente. Per rendere permanente un componente, impostare **msidbComponentAttributesPermanent** nella colonna Attributi della [tabella Component](component-table.md).

Si noti che il programma di installazione rimuove una chiave del Registro di sistema dopo la rimozione dell'ultimo valore o della sottochiave sotto la chiave. Per impedire la rimozione di una chiave del Registro di sistema vuota durante la disinstallazione, scrivere un valore fittizio nella chiave da mantenere e immettere + nella colonna Nome della tabella [Registro di sistema](registry-table.md).

 

 



