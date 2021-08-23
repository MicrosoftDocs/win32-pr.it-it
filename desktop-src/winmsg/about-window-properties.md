---
description: Questa panoramica illustra le proprietà della finestra.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Informazioni sulle proprietà della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c88657cba4cf12ed7ecedb07aeb545f8e4bf64109d34297637d734743d32dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028499"
---
# <a name="about-window-properties"></a>Informazioni sulle proprietà della finestra

Una *proprietà della finestra* è qualsiasi dato assegnato a una finestra. Una proprietà della finestra è in genere un handle dei dati specifici della finestra, ma può essere qualsiasi valore. Ogni proprietà della finestra è identificata da un nome di stringa. Esistono diverse funzioni che consentono alle applicazioni di usare le proprietà della finestra. Questa panoramica illustra gli argomenti seguenti:

-   [Vantaggi dell'uso delle proprietà della finestra](#advantages-of-using-window-properties)
-   [Assegnazione delle proprietà della finestra](#assigning-window-properties)
-   [Enumerazione delle proprietà della finestra](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Vantaggi dell'uso delle proprietà della finestra

Le proprietà della finestra vengono in genere usate per associare dati a una finestra sottoclassata o a una finestra in un'applicazione MDI (Multiple Document Interface). In entrambi i casi, non è utile usare i byte aggiuntivi specificati nella funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o nella struttura di classi per i due motivi seguenti:

-   Un'applicazione potrebbe non sapere quanti byte aggiuntivi sono disponibili o come viene usato lo spazio. Usando le proprietà della finestra, l'applicazione può associare i dati a una finestra senza accedere ai byte aggiuntivi.
-   Un'applicazione deve accedere ai byte aggiuntivi usando gli offset. Tuttavia, le proprietà della finestra sono accessibili dagli identificatori di stringa, non dagli offset.

Per altre informazioni sulla sottoclassazione, vedere [Creazione di sottoclassi di routine della finestra](about-window-procedures.md). Per altre informazioni sulle finestre MDI, vedere [Interfaccia a documenti multipli](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Assegnazione delle proprietà della finestra

La [**funzione SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) assegna una proprietà della finestra e il relativo identificatore di stringa a una finestra. La [**funzione GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) recupera la proprietà della finestra identificata dalla stringa specificata. La [**funzione RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) elimina l'associazione tra una finestra e una proprietà della finestra, ma non elimina i dati stessi. Per eliminare i dati stessi, usare la funzione appropriata per liberare l'handle restituito da **RemoveProp.**

## <a name="enumerating-window-properties"></a>Enumerazione delle proprietà della finestra

Le [**funzioni EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) ed [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enumerano tutte le proprietà di una finestra usando una funzione di callback definita dall'applicazione. Per altre informazioni sulla funzione di callback, vedere [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) include un parametro aggiuntivo per i dati definiti dall'applicazione usati dalla funzione di callback. Per altre informazioni sulla funzione di callback, vedere [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
