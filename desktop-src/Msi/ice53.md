---
description: ICE53 verifica la presenza di voci nella tabella Del Registro di sistema che scrivono informazioni sul programma di installazione privato o valori dei criteri nel Registro di sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d1e661eb832439a9b4fde423e005dc4b3a0c3ca9b266045c0ddd04daa63f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635132"
---
# <a name="ice53"></a>ICE53

ICE53 verifica la presenza di voci nella tabella Del Registro di sistema che scrivono informazioni sul programma di installazione privato o valori dei criteri nel Registro di sistema.

## <a name="result"></a>Risultato

ICE53 invia un avviso se la tabella Del Registro di sistema specifica la scrittura di informazioni interne o dei criteri nel Registro di sistema.

## <a name="example"></a>Esempio

ICE53 pubblica l'avviso seguente per l'esempio illustrato.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Tabella del Registro di](registry-table.md) sistema (parziale)



| Registro             | Radice         | Chiave                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registro di sistema1<br/> | 1<br/> | **Software** \\ **Criteri** \\ **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **DisableRollback**<br/> |



 

La riga della tabella del Registro di sistema 'Registry1' scrive un valore dei criteri di sistema nel Registro di sistema che influisce sull'installazione di tutti i pacchetti. A seconda del pacchetto, può essere possibile disabilitare il rollback solo per questo pacchetto impostando la [**proprietà DISABLEROLLBACK**](-disablerollback.md) nella [tabella Delle proprietà](property-table.md). Vedere [Rollback installation (Rollback dell'installazione).](rollback-installation.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




