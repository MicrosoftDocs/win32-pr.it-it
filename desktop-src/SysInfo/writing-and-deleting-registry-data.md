---
description: Un'applicazione può usare la funzione RegSetValueEx per associare un valore e i relativi dati a una chiave. Per un elenco dei tipi di valore supportati da RegSetValueEx, vedere tipi di valore del registro di sistema.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Scrittura ed eliminazione dei dati del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345031"
---
# <a name="writing-and-deleting-registry-data"></a>Scrittura ed eliminazione dei dati del registro di sistema

Un'applicazione può usare la funzione [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) per associare un valore e i relativi dati a una chiave. Per un elenco dei tipi di valore supportati da **RegSetValueEx**, vedere [tipi di valore del registro di sistema](registry-value-types.md).

Per eliminare un valore da una chiave, un'applicazione può usare la funzione [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) . Per eliminare una chiave, è possibile usare la funzione [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) . Una chiave eliminata non viene rimossa fino a quando non viene chiuso l'ultimo handle. Le sottochiavi e i valori non possono essere creati con una chiave eliminata.

Non è possibile bloccare una chiave del registro di sistema durante un'operazione di scrittura per sincronizzare l'accesso ai dati. Tuttavia, è possibile controllare l'accesso a una chiave del registro di sistema usando gli attributi di sicurezza. Per altre informazioni, vedere [sicurezza e diritti di accesso per la chiave del registro di sistema](registry-key-security-and-access-rights.md).

È possibile eseguire più di un'operazione del registro di sistema all'interno di una singola transazione. Per associare una chiave del registro di sistema a una transazione, un'applicazione può utilizzare la funzione [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) o [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) . Per ulteriori informazioni sulle transazioni, vedere [gestione transazioni kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
