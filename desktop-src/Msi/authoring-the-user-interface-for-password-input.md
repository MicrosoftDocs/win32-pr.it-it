---
description: Per ogni password che deve essere immessa dall'utente, aggiungere un controllo di modifica in una finestra di dialogo in cui è archiviato il valore della password in una proprietà.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Creazione dell'interfaccia utente per l'input della password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311029"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Creazione dell'interfaccia utente per l'input della password

Per ogni password che deve essere immessa dall'utente, aggiungere un controllo di modifica in una finestra di dialogo in cui è archiviato il valore della password in una proprietà. Questo [controllo di modifica](edit-control.md) deve avere l' [attributo di controllo password](password-control-attribute.md). Specifica che la proprietà immessa è una password e impedisce al programma di installazione di scrivere la proprietà nel file di log.

Gli [attributi del controllo](control-attributes.md) per il controllo di modifica della password sono MsidbControlAttributesVisible, MsidbControlAttributesEnabled e msidbControlAttributesPasswordInput (1 + 2 + 2097152). X, Y, larghezza, altezza e controllo \_ dipendono dal layout del controllo nella finestra di dialogo.

[Tabella di controllo](control-table.md)



| Finestra di dialogo\_ | controllo\_            | Tipo | X   | S   | Larghezza | Altezza | Attributi | Proprietà         | Testo | Controllo \_ successivo | Help |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordEdit | Modifica | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Annulla        |      |



 

Continuare a [proteggere l'installazione](securing-the-installation.md).

 

 



