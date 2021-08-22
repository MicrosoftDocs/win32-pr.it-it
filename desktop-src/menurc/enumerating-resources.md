---
title: Enumerazione delle risorse
description: In questo argomento vengono illustrate le funzioni usate per ottenere elenchi di risorse.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 6d3fbe60e3013fbeabdb21d74999040b51c42be2a1bb4521cda28a976bfe7aa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034339"
---
# <a name="enumerating-resources"></a>Enumerazione delle risorse

In determinate situazioni, potrebbe essere necessario individuare il contenuto delle risorse di un modulo PE (Portable Executable) sconosciuto. L Windows SDK fornisce funzioni di enumerazione delle risorse che consentono all'applicazione di ottenere elenchi di tipi di risorse, nomi e linguaggi in un modulo specificato.

* Le [**funzioni EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) [**ed EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) forniscono un elenco dei tipi di risorse presenti nel modulo.
* Le [**funzioni EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) [**ed EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) forniscono il nome di ogni risorsa all'interno di un determinato tipo.
* Le [**funzioni EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) ed [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) forniscono la lingua di ogni risorsa con un nome e un tipo specificato. 

Queste funzioni e le funzioni di callback associate consentono all'applicazione di creare un elenco di tutte le risorse in un modulo. Questo processo è descritto in [Creazione di un elenco di risorse](using-resources.md).

## <a name="-see-also"></a>-see-also

[Msistuff.exe'app di esempio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
