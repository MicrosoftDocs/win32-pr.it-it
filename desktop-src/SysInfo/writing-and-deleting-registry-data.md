---
description: Un'applicazione può usare la funzione RegSetValueEx per associare un valore e i relativi dati a una chiave. Per un elenco dei tipi di valore supportati da RegSetValueEx, vedere Tipi di valore del Registro di sistema.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Scrittura ed eliminazione di dati del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd4e80dc3320d1af0931e111c82f473e0edf56ac071443397ffc3da0918f7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883993"
---
# <a name="writing-and-deleting-registry-data"></a>Scrittura ed eliminazione di dati del Registro di sistema

Un'applicazione può usare [**la funzione RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) per associare un valore e i relativi dati a una chiave. Per un elenco dei tipi di valore supportati da **RegSetValueEx,** vedere [Tipi di valori del Registro di sistema.](registry-value-types.md)

Per eliminare un valore da una chiave, un'applicazione può usare la [**funzione RegDeleteValue.**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) Per eliminare una chiave, è possibile usare la [**funzione RegDeleteKey.**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) Una chiave eliminata non viene rimossa fino a quando non viene chiuso l'ultimo handle. Non è possibile creare sottochiavi e valori in una chiave eliminata.

Non è possibile bloccare una chiave del Registro di sistema durante un'operazione di scrittura per sincronizzare l'accesso ai dati. Tuttavia, è possibile controllare l'accesso a una chiave del Registro di sistema usando gli attributi di sicurezza. Per altre informazioni, vedere Sicurezza e diritti [di accesso delle chiavi del Registro di sistema.](registry-key-security-and-access-rights.md)

È possibile eseguire più di un'operazione del Registro di sistema all'interno di una singola transazione. Per associare una chiave del Registro di sistema a una transazione, un'applicazione può usare la funzione [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) o [**RegOpenKeyTransacted.**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) Per altre informazioni sulle transazioni, vedere [Gestione transazioni kernel.](/windows/desktop/Ktm/kernel-transaction-manager-portal)

 

 
