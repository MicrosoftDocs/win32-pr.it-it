---
description: Non è possibile accedere a una sessione del programma di installazione da un'azione personalizzata che non è la sessione di installazione corrente.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Accesso a un database o a una sessione dall'interno di un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c653d14bc2fdb361469389c4ee053e5d98b65f8c8265516c4e2c3bd4fc4c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046061"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Accesso a un database o a una sessione dall'interno di un'azione personalizzata

Non è possibile accedere a una sessione del programma di installazione da un'azione personalizzata che non è la sessione di installazione corrente. Le azioni personalizzate sono limitate all'uso solo del database attivo della sessione e nessun altro database. Le funzioni Windows [programma](database-functions.md) di installazione seguenti non devono essere chiamate da un'azione personalizzata, perché richiedono un handle per un database che non è il database della sessione di installazione corrente:

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alla sessione del programma di installazione corrente dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



