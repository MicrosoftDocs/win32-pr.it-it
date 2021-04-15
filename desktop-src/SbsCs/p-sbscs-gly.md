---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401578"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (applicazioni isolate e assembly side-by-side)

[A](a-sbscs-gly.md) B C [d](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configurazione per applicazione**
</dt> <dd>

Configurazione che può eseguire l'override della configurazione dell'applicazione globale di un assembly specifico. Una configurazione per applicazione è specificata da un file manifesto di configurazione dell'applicazione installato nella stessa cartella del file eseguibile. Il file manifesto descrive la versione o l'intervallo di versioni degli assembly affiancati che devono essere usati dall'applicazione. La configurazione per applicazione può essere usata quando una nuova versione di un assembly non è compatibile con un'applicazione. In questo caso, è possibile eseguire l'override della configurazione predefinita o globale dell'applicazione per un assembly affiancato specifico.

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly side-by-side privato**
</dt> <dd>

Un assembly side-by-side privato è visibile solo per un'applicazione specificata. Viene installato localmente in un'applicazione isolata e il codice dell'assembly diventa privato per il contesto dell'applicazione. Le dipendenze di un assembly side-by-side privato sono descritte nel file manifesto dell'applicazione. Gli assembly side-by-side privati possono essere usati per compensare gli effetti negativi della condivisione degli assembly, ad esempio i conflitti tra DLL e per semplificare la distribuzione dell'applicazione.

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**token di chiave pubblica**
</dt> <dd>

Stringa esadecimale a 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui è firmato l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per tutti gli assembly affiancati condivisi.

</dd> </dl>

 

 



