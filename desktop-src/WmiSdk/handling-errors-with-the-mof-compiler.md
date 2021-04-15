---
description: Se il compilatore MOF non è in grado di completare la compilazione di un file MOF, è possibile che il repository WMI rimanga in uno stato non definito.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Gestione degli errori con il compilatore MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485820"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Gestione degli errori con il compilatore MOF

Se il compilatore MOF non è in grado di completare la compilazione di un file MOF, è possibile che il repository WMI rimanga in uno stato non definito. Se, ad esempio, si compila un file MOF e si usa l'opzione della riga di comando **-Class: createonly** , la compilazione termina se esiste già una classe specificata nel file MOF. Il compilatore MOF archivia nel repository tutte le classi o istanze che sono state definite fino al punto in cui si interrompe il compilatore. In alcuni casi, è possibile lasciare il repository WMI in una condizione non definita.

In questa situazione, potrebbe essere necessario arrestare WMI, eliminare il repository WMI e ricompilarlo tramite WMI. Quando WMI viene riavviato, tutti i file MOF che contengono il comando [**pragma autocover**](pragma-autorecover.md) [preprocessore](preprocessor-commands.md) vengono ricompilati. È necessario ricompilare manualmente tutti i file MOF che non includono un' `#pragma autorecover` istruzione.

Per ulteriori informazioni su come dichiarare classi e istanze utilizzando la sintassi MOF, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di file MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



