---
description: Elenca le funzioni di accesso vettore fornite dalla libreria DirectXMath.
ms.assetid: 6e7453b8-0dee-6fc5-cbac-fe20e4e3ef60
title: Funzioni di accesso vettoriali della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a164375d23b15f02debcb110297f7fce63c6032eb5828acb8454b3bde4e7a846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118087802"
---
# <a name="directxmath-library-vector-accessor-functions"></a>Funzioni di accesso vettoriali della libreria DirectXMath

Elenca le funzioni di accesso vettore fornite dalla libreria DirectXMath.

Le funzioni di accesso vettoriale DirectXMath consentono agli sviluppatori di scrivere codice che ottiene e imposta singoli componenti di un vettore in modo portabile e ottimale.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                   | Descrizione                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorGetByIndex**](/previous-versions/windows/desktop/legacy/hh404786(v=vs.85))<br/>             | Recuperare il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati a virgola mobile in base all'indice.<br/>                                                                          |
| [**XMVectorGetByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetbyindexptr)<br/>       | Recuperare, in un'istanza di un tipo a virgola mobile a cui fa riferimento il puntatore, il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati a virgola mobile, a cui fa riferimento l'indice.<br/> |
| [**XMVectorGetIntByIndex**](/previous-versions/windows/desktop/legacy/hh404788(v=vs.85))<br/>       | Recuperare il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati integer in base all'indice.<br/>                                                                                 |
| [**XMVectorGetIntByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintbyindexptr)<br/> | Recuperare, in un'istanza di un integer a cui fa riferimento il puntatore, il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati integer in base all'indice.<br/>                          |
| [**XMVectorGetIntW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintw)<br/>                   | Recuperare il `w` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetIntWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintwptr)<br/>             | Recupera il componente di un tipo di dati XMVECTOR contenente dati integer e archivia il valore di tale componente in un'istanza di uint32 t a cui fa riferimento un `w` [](xmvector-data-type.md) \_ puntatore.<br/>                       |
| [**XMVectorGetIntX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintx)<br/>                   | Recuperare il `x` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetIntXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintxptr)<br/>             | Recupera il componente di un tipo di dati XMVECTOR contenente dati integer e archivia il valore di tale componente in un'istanza di uint32 t a cui fa riferimento un `x` [](xmvector-data-type.md) \_ puntatore.<br/>                       |
| [**XMVectorGetIntY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetinty)<br/>                   | Recuperare il `y` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetIntYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintyptr)<br/>             | Recupera il componente di un tipo di dati XMVECTOR contenente dati integer e archivia il valore di tale componente in un'istanza di uint32 t a cui fa riferimento un `y` [](xmvector-data-type.md) \_ puntatore.<br/>                       |
| [**XMVectorGetIntZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintz)<br/>                   | Recuperare il `z` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetIntZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintzptr)<br/>             | Recupera il componente di un tipo di dati XMVECTOR contenente dati integer e archivia il valore di tale componente in un'istanza di uint32 t a cui fa riferimento un `z` [](xmvector-data-type.md) \_ puntatore.<br/>                       |
| [**XMVectorGetW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetw)<br/>                         | Recuperare il `w` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetwptr)<br/>                   | Recuperare il componente di un tipo di dati XMVECTOR contenente dati a virgola mobile e archiviare il valore del componente in un'istanza di float a cui fa riferimento `w` un puntatore. [](xmvector-data-type.md)<br/>                    |
| [**XMVectorGetX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetx)<br/>                         | Recuperare il `x` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetxptr)<br/>                   | Recuperare il componente di un tipo di dati XMVECTOR contenente dati a virgola mobile e archiviare il valore del componente in un'istanza di float a cui fa riferimento `x` un puntatore. [](xmvector-data-type.md)<br/>                    |
| [**XMVectorGetY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgety)<br/>                         | Recuperare il `y` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetyptr)<br/>                   | Recuperare il componente di un tipo di dati XMVECTOR contenente dati a virgola mobile e archiviare il valore del componente in un'istanza di float a cui fa riferimento `y` un puntatore. [](xmvector-data-type.md)<br/>                    |
| [**XMVectorGetZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetz)<br/>                         | Recuperare il `z` componente di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**XMVectorGetZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetzptr)<br/>                   | Recuperare il componente di un tipo di dati XMVECTOR contenente dati a virgola mobile e archiviare il valore del componente in un'istanza di float a cui fa riferimento `z` un puntatore. [](xmvector-data-type.md)<br/>                    |
| [**XMVectorSetByIndex**](/previous-versions/windows/desktop/legacy/hh404810(v=vs.85))<br/>             | Usare un oggetto a virgola mobile per impostare il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati integer a cui fa riferimento un indice.<br/>                                         |
| [**XMVectorSetByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetbyindexptr)<br/>       | Usare un puntatore a un'istanza a virgola mobile per impostare il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati a virgola mobile a cui fa riferimento un indice.<br/>                   |
| [**XMVectorSetIntByIndex**](/previous-versions/windows/desktop/legacy/hh404813(v=vs.85))<br/>       | Usare un'istanza integer per impostare il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati integer a cui fa riferimento un indice.<br/>                                             |
| [**XMVectorSetIntByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintbyindexptr)<br/> | Usare un puntatore a un'istanza integer per impostare il valore di uno dei quattro componenti di un tipo di dati [**XMVECTOR**](xmvector-data-type.md) contenente dati integer a cui fa riferimento un indice.<br/>                                |
| [**XMVectorSetIntW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintw)<br/>                   | Impostare il valore del componente `w` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetIntWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintwptr)<br/>             | Imposta il `w` componente di un oggetto [**XMVECTOR**](xmvector-data-type.md) contenente dati integer, con un valore contenuto in un'istanza di uint32 t a cui fa \_ riferimento un puntatore.<br/>                                                 |
| [**XMVectorSetIntX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintx)<br/>                   | Impostare il valore del componente `x` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetIntXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintxptr)<br/>             | Imposta il `x` componente di un oggetto [**XMVECTOR**](xmvector-data-type.md) contenente dati integer, con un valore contenuto in un'istanza di uint32 t a cui fa \_ riferimento un puntatore.<br/>                                                 |
| [**XMVectorSetIntY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetinty)<br/>                   | Impostare il valore del componente `y` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetIntYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintyptr)<br/>             | Imposta il `y` componente di un oggetto [**XMVECTOR**](xmvector-data-type.md) contenente dati integer, con un valore contenuto in un'istanza di uint32 t a cui fa \_ riferimento un puntatore.<br/>                                                 |
| [**XMVectorSetIntZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintz)<br/>                   | Impostare il valore del componente `z` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetIntZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintzptr)<br/>             | Imposta il `z` componente di un oggetto [**XMVECTOR**](xmvector-data-type.md) contenente dati integer, con un valore contenuto in un'istanza di uint32 t a cui fa \_ riferimento un puntatore.<br/>                                                 |
| [**XMVectorSetW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetw)<br/>                         | Impostare il valore del componente `w` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetwptr)<br/>                   | Imposta il `w` componente di [**un XMVECTOR**](xmvector-data-type.md) contenente dati a virgola mobile, con un valore contenuto in un'istanza di float a cui fa riferimento un puntatore.<br/>                                              |
| [**XMVectorSetX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetx)<br/>                         | Impostare il valore del componente `x` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetxptr)<br/>                   | Imposta il `x` componente di [**un XMVECTOR**](xmvector-data-type.md) contenente dati a virgola mobile, con un valore contenuto in un'istanza di float a cui fa riferimento un puntatore.<br/>                                              |
| [**XMVectorSetY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsety)<br/>                         | Impostare il valore del componente `y` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetyptr)<br/>                   | Imposta il `y` componente di [**un XMVECTOR**](xmvector-data-type.md) contenente dati a virgola mobile, con un valore contenuto in un'istanza di float a cui fa riferimento un puntatore.<br/>                                              |
| [**XMVectorSetZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetz)<br/>                         | Impostare il valore del componente `z` di un tipo di dati [**XMVECTOR**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**XMVectorSetZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetzptr)<br/>                   | Imposta il `z` componente di [**un XMVECTOR**](xmvector-data-type.md) contenente dati a virgola mobile, con un valore contenuto in un'istanza di float a cui fa riferimento un puntatore.<br/>                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni della libreria DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
