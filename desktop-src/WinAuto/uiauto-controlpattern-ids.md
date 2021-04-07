---
title: Identificatori del pattern di controllo (UIAutomationClient. h)
description: Descrive le costanti denominate che identificano i pattern di controllo di automazione interfaccia utente Microsoft.
ms.assetid: 0192e840-96e6-4b12-a570-0d33a36ed885
topic_type:
- apiref
api_name:
- UIA_AnnotationPatternId
- UIA_CustomNavigationPatternId
- UIA_DockPatternId
- UIA_DragPatternId
- UIA_DropTargetPatternId
- UIA_ExpandCollapsePatternId
- UIA_GridItemPatternId
- UIA_GridPatternId
- UIA_InvokePatternId
- UIA_ItemContainerPatternId
- UIA_LegacyIAccessiblePatternId
- UIA_MultipleViewPatternId
- UIA_ObjectModelPatternId
- UIA_RangeValuePatternId
- UIA_ScrollItemPatternId
- UIA_ScrollPatternId
- UIA_SelectionItemPatternId
- UIA_SelectionPatternId
- UIA_SpreadsheetPatternId
- UIA_SpreadsheetItemPatternId
- UIA_StylesPatternId
- UIA_SynchronizedInputPatternId
- UIA_TableItemPatternId
- UIA_TablePatternId
- UIA_TextChildPatternId
- UIA_TextEditPatternId
- UIA_TextPatternId
- UIA_TextPattern2Id
- UIA_TogglePatternId
- UIA_TransformPatternId
- UIA_TransformPattern2Id
- UIA_ValuePatternId
- UIA_VirtualizedItemPatternId
- UIA_WindowPatternId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f17d668143beaed8000f99f761b84f5c193a51a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048569"
---
# <a name="control-pattern-identifiers"></a>Identificatori del pattern di controllo

Descrive le costanti denominate che identificano i pattern di controllo di automazione interfaccia utente Microsoft.



| Costante/valore                                                                                                                                                                                                                                                                                                               | Descrizione                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_AnnotationPatternId"></span><span id="uia_annotationpatternid"></span><span id="UIA_ANNOTATIONPATTERNID"></span><dl> <dt>**UIA \_ AnnotationPatternId**</dt> <dt>10023</dt> </dl>                             | Identifica il pattern di controllo dell' [annotazione](uiauto-implementingannotation.md) . Supportato a partire da Windows 8.<br/>                       |
| <span id="UIA_CustomNavigationPatternId"></span><span id="uia_customnavigationpatternid"></span><span id="UIA_CUSTOMNAVIGATIONPATTERNID"></span><dl> <dt>**UIA \_ CustomNavigationPatternId**</dt> <dt>10033</dt> </dl>     | Identifica il pattern di controllo [CustomNavigation](uiauto-implementingcustomnavigation.md) . Supportato a partire da Windows 10.<br/>          |
| <span id="UIA_DockPatternId"></span><span id="uia_dockpatternid"></span><span id="UIA_DOCKPATTERNID"></span><dl> <dt>**UIA \_ DockPatternId**</dt> <dt>10011</dt> </dl>                                                     | Identifica il pattern di controllo [Dock](uiauto-implementingdock.md) . <br/>                                                                     |
| <span id="UIA_DragPatternId"></span><span id="uia_dragpatternid"></span><span id="UIA_DRAGPATTERNID"></span><dl> <dt>**UIA \_ DragPatternId**</dt> <dt>10030</dt> </dl>                                                     | Identifica il pattern di controllo di [trascinamento](/windows/desktop/WinAuto/uiauto-implementingdrag) . Supportato a partire da Windows 8.<br/>                               |
| <span id="UIA_DropTargetPatternId"></span><span id="uia_droptargetpatternid"></span><span id="UIA_DROPTARGETPATTERNID"></span><dl> <dt>**UIA \_ DropTargetPatternId**</dt> <dt>10031</dt> </dl>                             | Identifica il pattern di controllo [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) . Supportato a partire da Windows 8.<br/>                   |
| <span id="UIA_ExpandCollapsePatternId"></span><span id="uia_expandcollapsepatternid"></span><span id="UIA_EXPANDCOLLAPSEPATTERNID"></span><dl> <dt>**UIA \_ ExpandCollapsePatternId**</dt> <dt>10005</dt> </dl>             | Identifica il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .<br/>                                                  |
| <span id="UIA_GridItemPatternId"></span><span id="uia_griditempatternid"></span><span id="UIA_GRIDITEMPATTERNID"></span><dl> <dt>**UIA \_ GridItemPatternId**</dt> <dt>10007</dt> </dl>                                     | Identifica il pattern di controllo [GridItem](uiauto-implementinggriditem.md) .<br/>                                                              |
| <span id="UIA_GridPatternId"></span><span id="uia_gridpatternid"></span><span id="UIA_GRIDPATTERNID"></span><dl> <dt>**UIA \_ GridPatternId**</dt> <dt>10006</dt> </dl>                                                     | Identifica il pattern di controllo [Grid](uiauto-implementinggrid.md) .<br/>                                                                      |
| <span id="UIA_InvokePatternId"></span><span id="uia_invokepatternid"></span><span id="UIA_INVOKEPATTERNID"></span><dl> <dt>**UIA \_ InvokePatternId**</dt> <dt>10000</dt> </dl>                                             | Identifica il pattern di controllo [Invoke](uiauto-implementinginvoke.md) .<br/>                                                                  |
| <span id="UIA_ItemContainerPatternId"></span><span id="uia_itemcontainerpatternid"></span><span id="UIA_ITEMCONTAINERPATTERNID"></span><dl> <dt>**UIA \_ ItemContainerPatternId**</dt> <dt>10019</dt> </dl>                 | Identifica il pattern di controllo [ItemContainer](uiauto-implementingitemcontainer.md) .<br/>                                                    |
| <span id="UIA_LegacyIAccessiblePatternId"></span><span id="uia_legacyiaccessiblepatternid"></span><span id="UIA_LEGACYIACCESSIBLEPATTERNID"></span><dl> <dt>**UIA \_ LegacyIAccessiblePatternId**</dt> <dt>10018</dt> </dl> | Identifica il pattern di controllo [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) .<br/>                                            |
| <span id="UIA_MultipleViewPatternId"></span><span id="uia_multipleviewpatternid"></span><span id="UIA_MULTIPLEVIEWPATTERNID"></span><dl> <dt>**UIA \_ MultipleViewPatternId**</dt> <dt>10008</dt> </dl>                     | Identifica il pattern di controllo [MultipleView](uiauto-implementingmultipleview.md) .<br/>                                                      |
| <span id="UIA_ObjectModelPatternId"></span><span id="uia_objectmodelpatternid"></span><span id="UIA_OBJECTMODELPATTERNID"></span><dl> <dt>**UIA \_ ObjectModelPatternId**</dt> <dt>10022</dt> </dl>                         | Identifica il pattern di controllo [ObjectModel](uiauto-implementingobjectmodel.md) . Supportato a partire da Windows 8.<br/>                     |
| <span id="UIA_RangeValuePatternId"></span><span id="uia_rangevaluepatternid"></span><span id="UIA_RANGEVALUEPATTERNID"></span><dl> <dt>**UIA \_ RangeValuePatternId**</dt> <dt>10003</dt> </dl>                             | Identifica il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) .<br/>                                                          |
| <span id="UIA_ScrollItemPatternId"></span><span id="uia_scrollitempatternid"></span><span id="UIA_SCROLLITEMPATTERNID"></span><dl> <dt>**UIA \_ ScrollItemPatternId**</dt> <dt>10017</dt> </dl>                             | Identifica il pattern di controllo [ScrollItem](uiauto-implementingscrollitem.md) .<br/>                                                          |
| <span id="UIA_ScrollPatternId"></span><span id="uia_scrollpatternid"></span><span id="UIA_SCROLLPATTERNID"></span><dl> <dt>**UIA \_ ScrollPatternId**</dt> <dt>10004</dt> </dl>                                             | Identifica il pattern di controllo [Scroll](uiauto-implementingscroll.md) .<br/>                                                                  |
| <span id="UIA_SelectionItemPatternId"></span><span id="uia_selectionitempatternid"></span><span id="UIA_SELECTIONITEMPATTERNID"></span><dl> <dt>**UIA \_ SelectionItemPatternId**</dt> <dt>10010</dt> </dl>                 | Identifica il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) .<br/>                                                    |
| <span id="UIA_SelectionPatternId"></span><span id="uia_selectionpatternid"></span><span id="UIA_SELECTIONPATTERNID"></span><dl> <dt>**UIA \_ SelectionPatternId**</dt> <dt>10001</dt> </dl>                                 | Identifica il pattern di controllo [Selection](uiauto-implementingselection.md) .<br/>                                                            |
| <span id="UIA_SpreadsheetPatternId"></span><span id="uia_spreadsheetpatternid"></span><span id="UIA_SPREADSHEETPATTERNID"></span><dl> <dt>**UIA \_ SpreadsheetPatternId**</dt> <dt>10026</dt> </dl>                         | Identifica il pattern di controllo del [foglio di calcolo](uiauto-implementingspreadsheet.md) . Supportato a partire da Windows 8.<br/>                     |
| <span id="UIA_SpreadsheetItemPatternId"></span><span id="uia_spreadsheetitempatternid"></span><span id="UIA_SPREADSHEETITEMPATTERNID"></span><dl> <dt>**UIA \_ SpreadsheetItemPatternId**</dt> <dt>10027</dt> </dl>         | Identifica il pattern di controllo [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) . Supportato a partire da Windows 8.<br/>             |
| <span id="UIA_StylesPatternId"></span><span id="uia_stylespatternid"></span><span id="UIA_STYLESPATTERNID"></span><dl> <dt>**UIA \_ StylesPatternId**</dt> <dt>10025</dt> </dl>                                             | Identifica il pattern di controllo [Styles](/windows/desktop/WinAuto/uiauto-implementingstyles) . Supportato a partire da Windows 8.<br/>                           |
| <span id="UIA_SynchronizedInputPatternId"></span><span id="uia_synchronizedinputpatternid"></span><span id="UIA_SYNCHRONIZEDINPUTPATTERNID"></span><dl> <dt>**UIA \_ SynchronizedInputPatternId**</dt> <dt>10021</dt> </dl> | Identifica il pattern di controllo [SynchronizedInput](uiauto-implementingsynchronizedinput.md) .<br/>                                            |
| <span id="UIA_TableItemPatternId"></span><span id="uia_tableitempatternid"></span><span id="UIA_TABLEITEMPATTERNID"></span><dl> <dt>**UIA \_ TableItemPatternId**</dt> <dt>10013</dt> </dl>                                 | Identifica il pattern di controllo [TableItem](uiauto-implementingtableitem.md) .<br/>                                                            |
| <span id="UIA_TablePatternId"></span><span id="uia_tablepatternid"></span><span id="UIA_TABLEPATTERNID"></span><dl> <dt>**UIA \_ TablePatternId**</dt> <dt>10012</dt> </dl>                                                 | Identifica il pattern di controllo [Table](uiauto-implementingtable.md) .<br/>                                                                    |
| <span id="UIA_TextChildPatternId"></span><span id="uia_textchildpatternid"></span><span id="UIA_TEXTCHILDPATTERNID"></span><dl> <dt>**UIA \_ TextChildPatternId**</dt> <dt>10029</dt> </dl>                                 | Identifica il pattern di controllo [TextChild](textchild-control-pattern.md) . Supportato a partire da Windows 8.<br/>                            |
| <span id="UIA_TextEditPatternId"></span><span id="uia_texteditpatternid"></span><span id="UIA_TEXTEDITPATTERNID"></span><dl> <dt>**UIA \_ TextEditPatternId**</dt> <dt>10032</dt> </dl>                                     | Identifica il pattern di controllo [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) . Supportato a partire da Windows 8.1.<br/>                    |
| <span id="UIA_TextPatternId"></span><span id="uia_textpatternid"></span><span id="UIA_TEXTPATTERNID"></span><dl> <dt>**UIA \_ TextPatternId**</dt> <dt>10014</dt> </dl>                                                     | Identifica il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) .<br/>                                                          |
| <span id="UIA_TextPattern2Id"></span><span id="uia_textpattern2id"></span><span id="UIA_TEXTPATTERN2ID"></span><dl> <dt>**UIA \_ TextPattern2Id**</dt> <dt>10024</dt> </dl>                                                 | Identifica la seconda versione del pattern di controllo [Text](uiauto-implementingtextandtextrange.md) . Supportato a partire da Windows 8.<br/> |
| <span id="UIA_TogglePatternId"></span><span id="uia_togglepatternid"></span><span id="UIA_TOGGLEPATTERNID"></span><dl> <dt>**UIA \_ TogglePatternId**</dt> <dt>10015</dt> </dl>                                             | Identifica il pattern di controllo dell' [interruttore](uiauto-implementingtoggle.md) .<br/>                                                                  |
| <span id="UIA_TransformPatternId"></span><span id="uia_transformpatternid"></span><span id="UIA_TRANSFORMPATTERNID"></span><dl> <dt>**UIA \_ TransformPatternId**</dt> <dt>10016</dt> </dl>                                 | Identifica il pattern di controllo [Transform](uiauto-implementingtransform.md) .<br/>                                                            |
| <span id="UIA_TransformPattern2Id"></span><span id="uia_transformpattern2id"></span><span id="UIA_TRANSFORMPATTERN2ID"></span><dl> <dt>**UIA \_ TransformPattern2Id**</dt> <dt>10028</dt> </dl>                             | Identifica la seconda versione del pattern di controllo [Transform](uiauto-implementingtransform.md) . Supportato a partire da Windows 8.<br/>   |
| <span id="UIA_ValuePatternId"></span><span id="uia_valuepatternid"></span><span id="UIA_VALUEPATTERNID"></span><dl> <dt>**UIA \_ ValuePatternId**</dt> <dt>10002</dt> </dl>                                                 | Identifica il pattern di controllo [value](uiauto-implementingvalue.md) .<br/>                                                                    |
| <span id="UIA_VirtualizedItemPatternId"></span><span id="uia_virtualizeditempatternid"></span><span id="UIA_VIRTUALIZEDITEMPATTERNID"></span><dl> <dt>**UIA \_ VirtualizedItemPatternId**</dt> <dt>10020</dt> </dl>         | Identifica il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .<br/>                                                |
| <span id="UIA_WindowPatternId"></span><span id="uia_windowpatternid"></span><span id="UIA_WINDOWPATTERNID"></span><dl> <dt>**UIA \_ WindowPatternId**</dt> <dt>10009</dt> </dl>                                             | Identifica il pattern di controllo [Window](uiauto-implementingwindow.md) .<br/>                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows XP \[ \| UWP\]<br/>                                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2003 \|\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

