---
description: Informazioni sui Windows Installer concetti che iniziano con la lettera D, ad esempio la funzione di database e la patch differenziale.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d76378d636c8ae14acdc9cb882c31840e3f1550f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010934"
---
# <a name="d-windows-installer"></a>D (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P Q](p-gly.md) [](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**funzione di database**
</dt> <dd>

Accede al database del programma di installazione. Queste funzioni vengono fornite principalmente [](i-gly.md) per l'uso da parte degli strumenti di creazione di pacchetti del programma di installazione e non devono essere usate per chiamare i servizi del programma di installazione. Per altre informazioni, vedere [Funzioni di database e](database-functions.md) Informazioni di riferimento sulle funzioni del programma di [installazione](installer-function-reference.md).

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**handle di database**
</dt> <dd>

Obbligatorio per l'uso di un database. Per altre informazioni, vedere [Recupero di un handle di database](obtaining-a-database-handle.md).

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**patch differenziale**
</dt> <dd>

Una patch differenziale è una patch Windows Installer compressa differenziale creata usando uno strumento, ad esempio Patchwiz.dll, che supporta la compressione differenziale. Le patch che usano la compressione differenziale possono ridurre le dimensioni di un aggiornamento fornendo solo le differenze (differenziali) tra i file esistenti in un computer di destinazione e i nuovi file desiderati. I nuovi file desiderati vengono quindi sintetizzati dai file esistenti e dai delta scaricati. Per altre informazioni sulla tecnologia di compressione differenziale, vedere [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).

</dd> </dl>

 

 



