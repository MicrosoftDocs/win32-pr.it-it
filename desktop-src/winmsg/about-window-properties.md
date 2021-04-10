---
description: In questa panoramica vengono illustrate le proprietà della finestra.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Informazioni sulle proprietà della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea646c594186b05bb74e70e6829f13a83cd0ec1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231585"
---
# <a name="about-window-properties"></a>Informazioni sulle proprietà della finestra

Una *proprietà della finestra* è qualsiasi dato assegnato a una finestra. Una proprietà della finestra è in genere un handle dei dati specifici della finestra, ma può essere qualsiasi valore. Ogni proprietà della finestra è identificata da un nome di stringa. Sono disponibili diverse funzioni che consentono alle applicazioni di utilizzare le proprietà della finestra. In questa panoramica vengono illustrati gli argomenti seguenti:

-   [Vantaggi dell'utilizzo delle proprietà della finestra](#advantages-of-using-window-properties)
-   [Assegnazione delle proprietà della finestra](#assigning-window-properties)
-   [Enumerazione delle proprietà della finestra](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Vantaggi dell'utilizzo delle proprietà della finestra

Le proprietà della finestra vengono in genere utilizzate per associare i dati a una finestra sottoclassata o a una finestra in un'applicazione con interfaccia a documenti multipli (MDI). In entrambi i casi, non è consigliabile usare i byte aggiuntivi specificati nella funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o nella struttura della classe per i due motivi seguenti:

-   Un'applicazione potrebbe non essere in grado di stabilire il numero di byte aggiuntivi disponibili o la modalità di utilizzo dello spazio. Utilizzando le proprietà della finestra, l'applicazione può associare dati a una finestra senza accedere ai byte aggiuntivi.
-   Un'applicazione deve accedere ai byte aggiuntivi tramite offset. Tuttavia, le proprietà della finestra sono accessibili in base ai relativi identificatori di stringa, non tramite offset.

Per ulteriori informazioni sulla sottoclasse, vedere la pagina relativa alla [sottoclasse della routine della finestra](about-window-procedures.md). Per ulteriori informazioni sulle finestre MDI, vedere [interfaccia a più documenti](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Assegnazione delle proprietà della finestra

La funzione [**seprop**](/windows/win32/api/winuser/nf-winuser-setpropa) assegna una proprietà della finestra e il relativo identificatore di stringa a una finestra. La funzione [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) recupera la proprietà della finestra identificata dalla stringa specificata. La funzione [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) Elimina l'associazione tra una finestra e una proprietà della finestra, ma non elimina i dati stessi. Per eliminare definitivamente i dati, usare la funzione appropriata per liberare l'handle restituito da **RemoveProp**.

## <a name="enumerating-window-properties"></a>Enumerazione delle proprietà della finestra

Le funzioni [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) e [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enumerano tutte le proprietà di una finestra utilizzando una funzione di callback definita dall'applicazione. Per ulteriori informazioni sulla funzione di callback, vedere [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) include un parametro aggiuntivo per i dati definiti dall'applicazione usati dalla funzione di callback. Per ulteriori informazioni sulla funzione di callback, vedere [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
