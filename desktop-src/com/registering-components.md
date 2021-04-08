---
title: Registrazione di componenti
description: Registrazione di componenti
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047401"
---
# <a name="registering-components"></a>Registrazione di componenti

Quando vengono installati i seguenti tipi di applicazioni, è necessario aggiungere le informazioni di installazione al registro di sistema, in genere tramite un programma di installazione:

-   Applicazioni server
-   Applicazioni contenitore/server
-   Applicazioni contenitore che consentono il collegamento a oggetti incorporati

Per tutte e tre le istanze, registrare le informazioni della libreria COM (DLL) e le informazioni specifiche dell'applicazione.

La DLL registra le informazioni per tutti i relativi componenti esportando [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Per registrare e annullare la registrazione di un componente, utilizzare le funzioni seguenti:

-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegSetValueEx**](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [**RegEnumKeyEx**](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 