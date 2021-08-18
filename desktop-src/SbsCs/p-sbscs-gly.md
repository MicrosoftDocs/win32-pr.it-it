---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc8e3d2591cfa1544ce11045f95df42e4a27d39b4a2b40d09bc3f2c907c2abec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142014"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (applicazioni isolate e assembly side-by-side)

[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configurazione per applicazione**
</dt> <dd>

Configurazione che può eseguire l'override della configurazione globale dell'applicazione di un assembly specifico. Una configurazione per applicazione viene specificata da un file manifesto di configurazione dell'applicazione installato nella stessa cartella del file eseguibile. Il file manifesto descrive la versione, o l'intervallo di versioni, degli assembly side-by-side che devono essere usati dall'applicazione. La configurazione per applicazione può essere usata quando una nuova versione di un assembly non è compatibile con un'applicazione. In questo caso, è possibile eseguire l'override della configurazione predefinita o globale dell'applicazione per un assembly side-by-side specifico.

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly side-by-side privato**
</dt> <dd>

Un assembly side-by-side privato è visibile solo a un'applicazione specificata. Viene installato in locale in un'applicazione isolata e il codice dell'assembly diventa privato per il contesto dell'applicazione. Le dipendenze di un assembly side-by-side privato sono descritte nel file manifesto dell'applicazione. Gli assembly side-by-side privati possono essere usati per compensare gli effetti negativi della condivisione di assembly, ad esempio conflitti di DLL, e per facilitare la distribuzione dell'applicazione.

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**token di chiave pubblica**
</dt> <dd>

Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica con cui viene firmato l'assembly. La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore. Obbligatorio per tutti gli assembly side-by-side condivisi.

</dd> </dl>

 

 



