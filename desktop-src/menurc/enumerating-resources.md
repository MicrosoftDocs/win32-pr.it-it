---
title: Enumerazione delle risorse
description: In questo argomento vengono illustrate le funzioni usate per ottenere elenchi di risorse.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910270"
---
# <a name="enumerating-resources"></a>Enumerazione delle risorse

In alcune situazioni può essere necessario individuare il contenuto delle risorse di un modulo PE (Portable Executable) sconosciuto. Il Windows SDK funzioni di enumerazione delle risorse che consentono all'applicazione di ottenere elenchi di tipi di risorse, nomi e linguaggi in un modulo specificato.

* Le [**funzioni EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) [**ed EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) forniscono un elenco dei tipi di risorse disponibili nel modulo.
* Le [**funzioni EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) ed [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) forniscono il nome di ogni risorsa all'interno di un determinato tipo.
* Le [**funzioni EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) ed [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) forniscono la lingua di ogni risorsa di un determinato nome e tipo. 

Queste funzioni e le funzioni di callback associate consentono all'applicazione di creare un elenco di tutte le risorse in un modulo. Questo processo è descritto in [Creazione di un elenco di risorse.](using-resources.md)

## <a name="-see-also"></a>-see-also

[Msistuff.exe app di esempio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
