---
title: Enumerazione delle risorse
description: In questo argomento vengono illustrate le funzioni utilizzate per ottenere elenchi di risorse.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ea7f2600f6da98cff6f16853092004a542b0f206
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323896"
---
# <a name="enumerating-resources"></a>Enumerazione delle risorse

In alcune situazioni, potrebbe essere necessario individuare il contenuto della risorsa di un modulo PE (Portable Executable) sconosciuto. Il Windows SDK fornisce funzioni di enumerazione delle risorse che consentono all'applicazione di ottenere elenchi di tipi di risorse, nomi e lingue in un modulo specificato.

* Le funzioni [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) e [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) forniscono un elenco di tipi di risorse disponibili nel modulo.
* Le funzioni [**EnumResourceNamesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) e [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) forniscono il nome di ogni risorsa all'interno di un determinato tipo.
* Le funzioni [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) e [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) forniscono la lingua di ogni risorsa di un determinato nome e tipo. 

Queste funzioni e le funzioni di callback associate consentono all'applicazione di creare un elenco di tutte le risorse in un modulo. Questo processo è descritto in [creazione di un elenco di risorse](using-resources.md).

## <a name="-see-also"></a>-vedere anche

[ App di esempioMsistuff.exe](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
