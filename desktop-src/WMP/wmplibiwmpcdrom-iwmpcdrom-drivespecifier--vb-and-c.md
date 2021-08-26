---
title: Proprietà driveSpecifier IWMPCdrom
description: La proprietà driveSpecifier ottiene la lettera di unità CD o DVD.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- Proprietà driveSpecifier Windows Media Player
- Proprietà driveSpecifier Windows Media Player, interfaccia IWMPCdrom
- Interfaccia IWMPCdrom Windows Media Player , proprietà driveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b555cba0ec694a19a01c040a0369aeb473c6811933d45892cbf3c69ef640b8b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031461"
---
# <a name="iwmpcdromdrivespecifier-property"></a>Proprietà IWMPCdrom::d riveSpecifier

La **proprietà driveSpecifier** ottiene la lettera di unità CD o DVD.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a>Valore proprietà

**System.String che** rappresenta la lettera di unità.

## <a name="remarks"></a>Commenti

In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD.

Questa proprietà ottiene una lettera di unità per un indice di unità in base zero all'interno dell'intervallo recuperato tramite **IWMPCdromCollection.count.** Il valore recuperato ha il formato *X*:, dove *X* rappresenta la lettera di unità.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

L'esempio seguente usa **driveSpecifier** per compilare una stringa che contiene un elenco di unità CD e DVD disponibili e visualizza tale stringa in una finestra di messaggio. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdromCollection.count (VB e C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





