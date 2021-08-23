---
description: Se il compilatore MOF non riesce a completare la compilazione di un file MOF, il repository WMI potrebbe essere lasciato in uno stato non definito.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Gestione degli errori con il compilatore MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f5174af836a0b27824c40486364cc81809db97b9608e6b1c813c4c1029d3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993171"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Gestione degli errori con il compilatore MOF

Se il compilatore MOF non riesce a completare la compilazione di un file MOF, il repository WMI potrebbe essere lasciato in uno stato non definito. Ad esempio, se si compila un file MOF e si usa l'opzione della riga di comando **-class:createonly,** la compilazione termina se esiste già una classe specificata nel file MOF. Il compilatore MOF archivia nel repository tutte le classi o le istanze definite fino al punto in cui il compilatore si arresta. In alcuni casi, questo può lasciare il repository WMI in una condizione non definita.

In questo caso, potrebbe essere necessario arrestare WMI, eliminare il repository WMI e ricompilarlo. Tutti i file MOF che contengono il comando del [preprocessore](preprocessor-commands.md) [**pragma autorecover**](pragma-autorecover.md) vengono ricompilati al riavvio di WMI. È necessario ricompilare manualmente tutti i file MOF che non includono `#pragma autorecover` un'istruzione .

Per altre informazioni su come dichiarare classi e istanze usando la sintassi MOF, vedere [Progettazione di Managed Object Format (CLASSI MOF).](designing-managed-object-format--mof--classes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di file MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



