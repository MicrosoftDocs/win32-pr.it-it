---
description: Per ogni password che deve essere immessa dall'utente, aggiungere un controllo di modifica in una finestra di dialogo che archivia il valore della password in una proprietà .
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Creazione del Interfaccia utente per l'input della password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b558243e24e4977d8e28311ac7643c118a26cdf62c89366694a16227b30c1969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066071"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Creazione del Interfaccia utente per l'input della password

Per ogni password che deve essere immessa dall'utente, aggiungere un controllo di modifica in una finestra di dialogo che archivia il valore della password in una proprietà . Questo [controllo di modifica](edit-control.md) deve avere l'attributo di controllo [password](password-control-attribute.md). Specifica che la proprietà immessa è una password e impedisce al programma di installazione di scrivere la proprietà nel file di log.

Gli [attributi di](control-attributes.md) controllo per il controllo di modifica della password sono msidbControlAttributesVisible, msidbControlAttributesEnabled e msidbControlAttributesPasswordInput (1 + 2 + 2097152). X, Y, Width, Height e Control Next dipendono dal \_ layout del controllo nella finestra di dialogo.

[Tabella di controllo](control-table.md)



| Finestra di dialogo\_ | controllo\_            | Tipo | X   | S   | Larghezza | Altezza | Attributi | Proprietà         | Testo | Controllo \_ successivo | Help |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordModifica | Modifica | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Annulla        |      |



 

Continuare con [Protezione dell'installazione](securing-the-installation.md).

 

 



