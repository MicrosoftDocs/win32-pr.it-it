---
description: La funzione di esportazione FormatProperties formatta i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor. Se si desidera visualizzare i dati nel riquadro dei dettagli, è necessario implementare la funzione di esportazione FormatProperties in tutte le dll del parser.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Funzione di callback FormatProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305929"
---
# <a name="formatproperties-callback-function"></a>Funzione di callback FormatProperties

La funzione di esportazione **FormatProperties** formatta i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor. Se si desidera visualizzare i dati nel riquadro dei dettagli, è necessario implementare la funzione di esportazione **FormatProperties** in tutte le dll del parser.

## <a name="syntax"></a>Sintassi


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame da analizzare.

</dd> <dt>

*lpFrame* \[ in\]
</dt> <dd>

Puntatore al primo byte di un frame.

</dd> <dt>

*lpProtocol* \[ in\]
</dt> <dd>

Puntatore all'inizio dei dati del protocollo in un frame.

</dd> <dt>

*nPropertyInsts* \[ in\]
</dt> <dd>

Numero di strutture [PROPERTYINST](propertyinst.md) fornite da *lpPropInst*.

</dd> <dt>

*lpPropInst* \[ in\]
</dt> <dd>

Puntatore a una matrice di strutture [PROPERTYINST](propertyinst.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Network Monitor chiama la funzione **FormatProperties** per visualizzare i dati nel riquadro dei dettagli dell'interfaccia utente Network Monitor. In genere, **FormatProperties** viene chiamato per formattare la riga di riepilogo per un protocollo e quindi per formattare tutte le istanze di proprietà del protocollo all'interno di un frame. Tuttavia, Network Monitor non garantisce il numero di volte che chiama **FormatProperties** per un parser specifico.

Durante l'implementazione della funzione **FormatProperties** , il parser chiama indirettamente la funzione [FormatPropertyInstance](formatpropertyinstance.md) per usare il formattatore generico fornito da Network Monitor oppure può chiamare una routine di formattatore personalizzata definita dal parser. È necessario chiamare uno dei formattatori per ogni struttura [PROPERTYINST](propertyinst.md) passata alla DLL del parser nel parametro *lpPropInst* .



| Per informazioni su                                          | Vedere                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor.   | [Parser](parsers.md)                                             |
| I punti di ingresso inclusi nella DLL del parser.          | [Architettura DLL parser](parser-dll-architecture.md)             |
| L'implementazione di **FormatProperties**  include un esempio. | [Implementazione di FormatProperties](implementing-formatproperties.md) |
| In che modo il formattatore generico formatta tipi diversi di dati.  | [Output formattatore generico](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




