---
title: Interfacce di transizione
description: Questa sezione contiene le specifiche di riferimento per le Windows di Animation Manager che supportano le transizioni.
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5791de6e2ca148e42ef836c8bb9be2d9dc96304df00a856b1bc036e05fca3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418601"
---
# <a name="transition-interfaces"></a>Interfacce di transizione

Questa sezione contiene le specifiche di riferimento per le Windows di Animation Manager che supportano le transizioni.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                     | Descrizione                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | Definisce i metodi per la creazione di un interpolatore personalizzato.<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | Estende [**l'interfaccia IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) che definisce i metodi per la creazione di un interpolatore personalizzato. [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) supporta l'interpolazione in una determinata dimensione. <br/>        |
| [**IUIAnimationPrimitiveInterpolation**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | Definisce un metodo che consente a un interpolatore personalizzato di fornire informazioni sulla transizione, sotto forma di curva polinomiale cubica, al gestore dell'animazione.<br/>                                                                                                        |
| [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | Definisce una transizione che determina il modo in cui una variabile di animazione cambia nel tempo.<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | Estende [**l'interfaccia IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) che definisce una transizione. Una [**transizione IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2) determina il modo in cui una variabile di animazione cambia nel tempo in una determinata dimensione.<br/> |
| [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | Definisce un metodo per la creazione di transizioni da interpolatori personalizzati.<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | Definisce un metodo per la creazione di transizioni da interpolatori personalizzati.<br/>                                                                                                                                                                                            |
| [**Libreria IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | Definisce una libreria di transizioni standard. <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | Definisce una libreria di transizioni standard per una dimensione specificata.<br/>                                                                                                                                                                                            |
| [**IUIAnimationVariable**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | Definisce una variabile di animazione, che rappresenta un elemento visivo che può essere animato.<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | Definisce una variabile di animazione, che rappresenta un elemento visivo che può essere animato in più dimensioni.<br/>                                                                                                                                                   |
| [**IUIAnimationVariableChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | Definisce un metodo per la gestione degli eventi correlati agli aggiornamenti delle variabili di animazione.<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | Definisce un metodo per la gestione degli eventi di aggiornamento delle variabili di animazione. [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) gestisce gli eventi che si verificano in una dimensione specificata.<br/>                                                            |
| [**IUIAnimationVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | Definisce un metodo per la gestione degli eventi di aggiornamento delle variabili di animazione.<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | Definisce un metodo per la gestione degli eventi di aggiornamento delle variabili di animazione. [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) gestisce gli eventi che si verificano in una dimensione specificata.<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | Definisce un metodo per la gestione degli eventi di aggiornamento della curva di animazione. <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce](windows-animation-reference.md)
</dt> </dl>

 

 





