---
title: Allocazione di ID WinEvent
description: Ogni WinEvent è destinato a essere usato solo per uno scopo specifico. L'uso di un WinEvent per uno scopo imprevisto può causare conflitti con altre applicazioni o il sistema operativo, il che può comportare l'instabilità delle applicazioni o del sistema operativo.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f339641e5a3b679f572bc3b60c3e68be7b65f2a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299841"
---
# <a name="allocation-of-winevent-ids"></a>Allocazione di ID WinEvent

Ogni WinEvent è destinato a essere usato solo per uno scopo specifico. L'uso di un WinEvent per uno scopo imprevisto può causare conflitti con altre applicazioni o il sistema operativo, il che può comportare l'instabilità delle applicazioni o del sistema operativo.

Microsoft ha definito diverse categorie di WinEvents e, per ogni categoria, ha definito uno o più intervalli di valori da usare come ID WinEvent. L'intervallo riservato della community (0xA000-0xAFFF) è disponibile per le applicazioni che devono definire nuovi WinEvents. L'utilizzo di valori da questo intervallo consente di ridurre il rischio di collisioni. Tuttavia, gli sviluppatori che creano nuovi WinEvents devono ancora collaborare per evitare conflitti tra le applicazioni.

Nella tabella seguente vengono illustrate le categorie WinEvent e gli intervalli di valori definiti per ogni categoria.



| Category                                                | Range         | Attualmente in uso | Commenti                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Eventi di Microsoft Active Accessibility (sistema riservato) | 0x0001-0x00FF | 0x0001-0x0020    | \_ \_ \* ID evento sistema eventi                                                                     |
| Eventi di Microsoft Active Accessibility (sistema riservato) | 0x4001-0x40FF | 0x4001-0x4007    | \_ \_ \* ID evento Console eventi                                                                    |
| Eventi di automazione interfaccia utente (sistema riservato)                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | ID evento di automazione interfaccia utente                                                                         |
| Eventi di automazione interfaccia utente (sistema riservato)                  | 0x7500-0x75FF | 0x7530-0x759B    | ID evento di modifica proprietà di automazione interfaccia utente                                                        |
| Eventi di Microsoft Active Accessibility (sistema riservato) | 0x8000-0x80FF | 0x8000-0x8015    | \_ \_ \* ID evento oggetto evento                                                                     |
| OEM riservato                                            | 0x0101-0x01FF | 0x0101-0x0122    | ID evento IAccessible2                                                                          |
| Community riservata                                      | 0xA000-0xAFFF | nessuno             | Riservato per i nuovi eventi definiti dalle specifiche AIA (Accessibility Interoperability Alliance) |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | Riservato per eventi personalizzati allocati in fase di esecuzione                                                 |



 

Gli argomenti seguenti descrivono gli intervalli di WinEvent in modo più dettagliato.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Eventi di Microsoft Active Accessibility e automazione interfaccia utente

Cinque intervalli di ID WinEvent sono riservati per l'uso da Microsoft Active Accessibility e dall'automazione interfaccia utente Microsoft. Il primo intervallo (0x0001-0x00FF) è riservato per gli eventi a livello di sistema, in genere utilizzati per descrivere le situazioni che interessano tutte le applicazioni nel sistema. Il secondo intervallo (0x4001-0x40FF) è riservato per gli eventi specifici di Windows Console. Il terzo intervallo (0x4E00-0x4EFF) e quarto intervallo (0x7500-0x75FF) sono per la reflection degli eventi di automazione interfaccia utente. Infine, il quinto intervallo (0x8000-0x80FF) è per gli eventi a livello di oggetto che riguardano situazioni specifiche di oggetti all'interno di un'applicazione.

Tutti gli eventi di Microsoft Active Accessibility e di automazione interfaccia utente sono definiti nei file di intestazione WinUser. h e UIAutomationClient. h.

## <a name="oem-reserved-events"></a>Eventi riservati OEM

L'intervallo riservato OEM è aperto a chiunque debba utilizzare WinEvents come meccanismo di comunicazione. Gli sviluppatori devono definire e pubblicare le definizioni degli eventi insieme ai relativi parametri (o anche ai tipi di oggetto associati) per l'elaborazione degli eventi, in modo che sia possibile evitare conflitti accidentali di ID evento. La specifica IAccessible2 utilizza parte dell'intervallo riservato OEM.

## <a name="community-reserved-events"></a>Eventi riservati della community

L'intervallo riservato della community è per WinEvents specificato da Accessibility Interoperability Alliance (AIA) per l'uso in tutto il settore. Gli sviluppatori sono vivamente invitati a definire e pubblicare una specifica ufficiale prima di usare i valori di questo intervallo.

## <a name="atom-events"></a>Eventi ATOM

L'intervallo ATOM è riservato agli ID evento allocati in fase di esecuzione tramite l'API di estendibilità di automazione interfaccia utente. Non utilizzare i valori dell'intervallo ATOM per altri scopi. L'utilizzo della funzione [**GlobalAddAtom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) con un GUID di stringa è il metodo consigliato per l'allocazione di WinEvents dall'intervallo Atom.

## <a name="using-values-from-a-reserved-range"></a>Utilizzo di valori da un intervallo riservato

In base alla specifica WinEvent, i valori dell'intervallo riservato di sistema o di qualsiasi altro intervallo non definito non possono essere usati senza modificare l'SDK. Per le nuove WinEvents, le applicazioni devono usare i valori degli intervalli riservati OEM riservati o della community. Prima di usare un nuovo WinEvent, gli sviluppatori sono fortemente invitati a condividere le specifiche in modo aperto e ampio e dovrebbero collaborare con l'alleanza di interoperabilità di accessibilità per definire le specifiche di WinEvent.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Alleanza di interoperabilità per l'accessibilità](https://www.atia.org/)
</dt> </dl>

 

 