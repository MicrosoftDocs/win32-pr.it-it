---
description: ICE53 verifica la presenza di voci nella tabella del registro di sistema che scrivono le informazioni sul programma di installazione privato o i valori dei criteri nel registro di sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315905"
---
# <a name="ice53"></a>ICE53

ICE53 verifica la presenza di voci nella tabella del registro di sistema che scrivono le informazioni sul programma di installazione privato o i valori dei criteri nel registro di sistema.

## <a name="result"></a>Risultato

ICE53 pubblica un avviso se la tabella del registro di sistema specifica la scrittura delle informazioni interne o dei criteri nel registro di sistema.

## <a name="example"></a>Esempio

ICE53 invia l'avviso seguente per l'esempio illustrato.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Tabella del registro di sistema](registry-table.md) (parziale)



| Registro             | Radice         | Chiave                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Software** \\ di **Criteri** \\ di **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **DisableRollback**<br/> |



 

La riga della tabella del registro di sistema ' Registry1' scrive un valore dei criteri di sistema nel registro di sistema che influiscono sull'installazione di tutti i pacchetti. A seconda del pacchetto, può essere possibile disabilitare il rollback solo per questo pacchetto impostando la proprietà [**DisableRollback**](-disablerollback.md) nella [tabella delle proprietà](property-table.md). Vedere eseguire il [rollback dell'installazione](rollback-installation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




