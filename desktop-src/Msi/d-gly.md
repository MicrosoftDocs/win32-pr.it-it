---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752319"
---
# <a name="d-windows-installer"></a>D (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) d [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**funzione di database**
</dt> <dd>

Accede al database del programma di installazione. Queste funzioni vengono fornite principalmente dagli strumenti di [*creazione dei pacchetti del programma di installazione*](i-gly.md) e non sono progettate per essere usate per chiamare i servizi del programma di installazione. Per ulteriori informazioni, vedere [funzioni di database](database-functions.md) e [riferimento](installer-function-reference.md)alle funzioni del programma di installazione.

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**handle di database**
</dt> <dd>

Obbligatorio per l'utilizzo di un database. Per ulteriori informazioni, vedere [ottenere un handle di database](obtaining-a-database-handle.md).

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**patch Delta**
</dt> <dd>

Una patch Delta è una patch Windows Installer compressa Delta creata usando uno strumento, ad esempio Patchwiz.dll, che supporta la compressione delta. Le patch che usano la compressione delta possono ridurre le dimensioni di un aggiornamento fornendo solo le differenze (Delta) tra i file esistenti in un computer di destinazione e i nuovi file desiderati. I nuovi file desiderati vengono quindi sintetizzati dai file esistenti e dai Delta scaricati. Per ulteriori informazioni sulla tecnologia di compressione Delta, vedere l' [interfaccia di programmazione dell'applicazione di compressione delta](https://msdn.microsoft.com/library/ms811406.aspx).

</dd> </dl>

 

 



